# LP-CA: Emergent Left-Periphery Word Order Simulation

This repository contains a **NetLogo** implementation of a local-interaction model for left-peripheral word order.
The model tests whether correct surface configurations can emerge **without** a fixed global template, using only local precedence rules and local compatibility constraints.

The simulation implements two reference hierarchies:

* **Frascarelli (2012)**
* **Rizzi & Bocci (2017)**

and two update modes:

* **Cascade** – revisits earlier constituents and may update earlier adjacent pairs
* **Pairwise** – evaluates one fixed adjacent pair per step; earlier placements remain fixed

The repository contains two versions of the model:

* `JLM_simulation_Frascarelli2012+Rizzi2017B.nlogo`
  Interactive version of the simulation, for manual exploration in NetLogo Desktop or NetLogo Web.

* `LP_word_order_batch (2).nlogo`
  Batch-testing version of the simulation, intended for automated experiments using NetLogo BehaviorSpace.

---

## Running the Interactive Model

Use the interactive model file:

```bash
JLM_simulation_Frascarelli2012+Rizzi2017B.nlogo
```

### Option 1 – NetLogo Desktop

1. Download and install [NetLogo](https://ccl.northwestern.edu/netlogo/) version 6.x or later.

2. Download this repository:

   ```bash
   git clone https://github.com/linguisticsnet/netlogo-anon-model.git
   ```

   or click **Code → Download ZIP** and extract it.

3. Open `JLM_simulation_Frascarelli2012+Rizzi2017B.nlogo` in NetLogo.

4. In the **Interface** tab:

   * Set `reference-model` to **Frascarelli 2012** or **Rizzi & Bocci 2017**
   * Set `update-method` to **Cascade** or **Pairwise**
   * Click `setup` to create a random valid starting row
   * Click `setup-manual` to enter your own initial sequence
   * Click `setup-predefined` to load a fixed test pattern
   * Click `go` to run the simulation

### Option 2 – NetLogo Web

The interactive version can also be run in the browser:

1. Go to [NetLogo Web](https://www.netlogoweb.org/launch#)
2. Click **Upload model**
3. Select `JLM_simulation_Frascarelli2012+Rizzi2017B.nlogo`
4. Run the simulation as in the desktop version

> **Note:** If labels do not display correctly in NetLogo Web, uncomment the web-compatible `update-label` procedure included in the code.

---

## Running Batch Experiments

Use the batch-testing model file:

```bash
LP_word_order_batch (2).nlogo
```

> **Important:** Batch experiments can only be executed in the **NetLogo Desktop** application.
> NetLogo Web does not support BehaviorSpace batch execution.

### Running a BehaviorSpace Experiment

1. Open NetLogo Desktop.

2. Open `LP_word_order_batch (2).nlogo`.

3. Go to **Tools → BehaviorSpace**.

4. Create a new experiment or select an existing predefined experiment.

5. Choose which model parameters to vary, for example:

   * `reference-model`
   * `update-method`
   * number of repetitions
   * stopping condition
   * output variables to record

6. Specify the number of repetitions for each condition, e.g. 50.

7. Select the output measures to save, such as:

   * success or failure of the run
   * initial configuration
   * final configuration
   * number of update steps

8. Click **Run**.

9. Choose an output file location.

10. Run the experiment and analyze the exported results.


---

Happy modeling!
