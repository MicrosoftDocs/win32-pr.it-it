---
title: Porting di funzioni di illuminazione e materiali
description: Le funzioni OpenGL per l'illuminazione e i materiali differiscono sostanzialmente dalle funzioni di IRIS GL. Diversamente da IRIS GL, OpenGL dispone di funzioni separate per l'impostazione di luci, modelli leggeri e materiali.
ms.assetid: de57d041-1ea1-46d0-b584-009608625ea5
keywords:
- Porting di IRIS GL, illuminazione
- porting da IRIS GL, illuminazione
- porting in OpenGL da IRIS GL, illuminazione
- Porting OpenGL da IRIS GL, illuminazione
- Porting, materiali di IRIS GL
- porting da IRIS GL, Materials
- porting in OpenGL da IRIS GL, Materials
- Porting OpenGL da IRIS GL, Materials
- illuminazione
- materiali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c775670b7ae49e41fed35c192385c72e72e880b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856537"
---
# <a name="porting-lighting-and-materials-functions"></a>Porting di funzioni di illuminazione e materiali

Le funzioni OpenGL per l'illuminazione e i materiali differiscono sostanzialmente dalle funzioni di IRIS GL. Diversamente da IRIS GL, OpenGL dispone di funzioni separate per l'impostazione di luci, modelli leggeri e materiali.

Quando si trasportano funzioni di illuminazione e materiali, tenere presenti i seguenti aspetti:

-   OpenGL non contiene tabelle di definizioni archiviate. È possibile usare gli elenchi di visualizzazione per simulare il meccanismo def/bind di IRIS GL. Per altre informazioni su defs e binding, vedere [porting defs, binds e sets](porting-defs--binds--and-sets.md).
-   Con OpenGL, l'attenuazione è associata a ogni sorgente di luce, anziché al modello di illuminazione generale.
-   I componenti diffusi e speculari sono separati nelle fonti di luce OpenGL.
-   Le fonti di luce OpenGL includono un componente alfa. Quando si porta il codice IRIS GL, impostare questo componente alfa su 1,0, che indica il 100% opaco. I valori alfa vengono quindi determinati solo dal componente alfa dei materiali, quindi gli oggetti nella scena avranno un aspetto analogo a quello di IRIS GL.

Nella tabella seguente sono elencate le funzioni di illuminazione e materiali IRIS GL e le relative funzioni OpenGL equivalenti.



| Funzione IRIS GL                 | OpenGL (funzione)                               | Significato                                                       |
|----------------------------------|-----------------------------------------------|---------------------------------------------------------------|
| **Imdef (deflight**,... **)**    | [glLight](gllight-functions.md)              | Definire una sorgente di luce.                                        |
| **Imdef (DEFLMODEL**,... **)**   | [glLightModel](gllightmodel-functions.md)    | Definire un modello di illuminazione.                                      |
| **Annulla binding**                       | [**glEnable**](glenable.md) (GL \_ Light *i*) | Abilita la luce *i*.                                             |
| **Annulla binding**                       | **glEnable**( \_ illuminazione GL)                  | Abilita illuminazione.                                              |
| **Imdef (DEFMATERIAL**,... **)** | [**glMaterial**](glmaterial-functions.md)    | Definire un materiale.                                            |
| **Imcolore**                      | [**glColorMaterial**](glcolormaterial.md)    | Modificare l'effetto dei comandi colore mentre l'illuminazione è attiva. |
|                                  | [**glGetMaterial**](glgetmaterial.md)        | Ottenere i parametri del materiale.                                      |



 

La tabella seguente elenca diversi parametri del materiale IRIS GL e i parametri OpenGL equivalenti.



| Indice Imdef  | parametro glMaterial                              | Predefinito              | Significato                                                                                       |
|--------------|---------------------------------------------------|----------------------|-----------------------------------------------------------------------------------------------|
| Alfa        | GL \_ diffuse                                       |                      | Il quarto valore nel parametro GL \_ Diffusion specifica il valore alfa.                      |
| AMBIENTE      | \_ambiente GL                                       | (0,2, 0,2, 0,2, 1,0) | Colore ambiente.                                                                                |
| CON riflessione diffusa      | GL \_ diffuse                                       | (0,8, 0,8, 0,8, 1,0) | Colore diffuso.                                                                                |
| SPECULARE     | \_speculare GL                                      | (0,0, 0,0, 0,0, 1,0) | Colore emissivo.                                                                               |
| LUCENTEZZA    | GL \_ SHININESSGL \_ ambiente \_ e \_ diffusa<br/> | 0,0                  | Esponente speculare. Equivale a chiamare due volte **glMaterial** con gli stessi valori.<br/> |
| COLORINDEXES | indici di \_ colore GL \_                                |                      | Indici di colore per l'illuminazione ambiente, diffusa e speculare.                                    |



 

Quando il primo parametro di **Imdef** è DEFMODEL, la traduzione OpenGL equivalente è la funzione [**glLightModel**](gllightmodel-functions.md). L'eccezione si verifica quando il parametro che segue DEFMODEL è ATTENUAzione: quindi la funzione OpenGL equivalente è [**glLight**](gllight-functions.md).

La tabella seguente elenca i parametri del modello di illuminazione equivalente per IRIS GL e OpenGL.



| Indice Imdef | parametro glLightModel          | Predefinito              | Significato                                          |
|-------------|---------------------------------|----------------------|--------------------------------------------------|
| AMBIENTE     | \_ \_ ambiente modello di luce GL \_       | (0,2, 0,2, 0,2, 1,0) | Colore ambiente della scena.                          |
| ATTENUAZIONE |                                 |                      | Vedere [**glLight**](gllight-functions.md).        |
| LOCALVIEWER | \_ \_ \_ Visualizzatore locale del modello GL Light \_ | GL \_ false            | Visualizzatore locale (**true**) o infinito (**false**). |
| TWOSIDE     | GL \_ LIGHTMODEL \_ due \_ lati       | GL \_ false            | Usare l'illuminazione a due lati se **true**.            |



 

Quando il primo parametro di **Imdef** è deflight, la traduzione OpenGL equivalente è la funzione [**glLight**](gllight-functions.md) .

La tabella seguente elenca i parametri di illuminazione equivalenti per IRIS GL e OpenGL.



| Indice Imdef           | parametro glLight                                                                                 | Predefinito                                                                             | Significato                                                                        |
|-----------------------|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| AMBIENTE               | \_AMBIENTGL \_ diffusa<br/> \_speculare GL<br/>                                         | (0,0, 0,0, 0,0, 1,0) (1,0, 1,0, 1,0, 1,0)<br/> (1,0, 1,0, 1,0, 1,0)<br/> | Intensità di ambiente. Intensità diffusa.<br/> Intensità speculare.<br/> |
| LCOLOR                | Nessun equivalente.                                                                                    |                                                                                     |                                                                                |
| POSITION              | \_posizione GL                                                                                      | (0,0, 0,0, 1,0, 0,0)                                                                | Posizione della luce.                                                             |
| SPOTDIRECTION         | \_direzione spot \_ GL                                                                               | (0, 0, 1)                                                                           | Direzione del riflettore.                                                        |
| RIFLETTORI             | \_cutoff spot \_ EXPONENTGL \_ spot \_<br/>                                                     | 0180<br/>                                                                     | Distribuzione dell'intensità. Angolo massimo spread della sorgente di luce.<br/>        |
| DEFMODEL, ATTENUAZIONE | \_ \_ \_ attenuazione lineare ATTENUATIONGL costante GL \_<br/> \_attenuazione quadratica GL \_<br/> | (1, 0, 0)                                                                           | Fattori di attenuazione.                                                           |



 

 

 





