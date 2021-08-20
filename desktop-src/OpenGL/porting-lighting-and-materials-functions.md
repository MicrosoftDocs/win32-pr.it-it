---
title: Funzioni di porting di illuminazione e materiali
description: Le funzioni OpenGL per l'illuminazione e i materiali sono sostanzialmente diverse dalle funzioni IRIS GL. A differenza di IRIS GL, OpenGL ha funzioni separate per l'impostazione di luci, modelli di luce e materiali.
ms.assetid: de57d041-1ea1-46d0-b584-009608625ea5
keywords:
- Porting IRIS GL, illuminazione
- porting da IRIS GL, illuminazione
- porting a OpenGL da IRIS GL, illuminazione
- Porting OpenGL da IRIS GL, illuminazione
- Porting IRIS GL, materiali
- porting da IRIS GL, materiali
- porting a OpenGL da IRIS GL, materiali
- Porting OpenGL da IRIS GL, materiali
- illuminazione
- Materiali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45041dde0902f983648c6d258f4c4a8220085d0d8bbeddc6fbdbc970033a50ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118933031"
---
# <a name="porting-lighting-and-materials-functions"></a>Funzioni di porting di illuminazione e materiali

Le funzioni OpenGL per l'illuminazione e i materiali sono sostanzialmente diverse dalle funzioni IRIS GL. A differenza di IRIS GL, OpenGL ha funzioni separate per l'impostazione di luci, modelli di luce e materiali.

Quando si esegue il porting delle funzioni di illuminazione e materiali, tenere presente quanto segue:

-   OpenGL non include alcuna tabella di definizioni archiviate. È possibile usare gli elenchi di visualizzazione per simulare il meccanismo di def/binding IRIS GL. Per altre informazioni su def e associazioni, vedere [Porting Defs, Binds, and Sets](porting-defs--binds--and-sets.md).
-   Con OpenGL, l'attenuazione è associata a ogni sorgente di luce, anziché al modello di illuminazione complessivo.
-   I componenti diffusi e speculari sono separati nelle sorgenti di luce OpenGL.
-   Le sorgenti di luce OpenGL hanno un componente alfa. Quando si esegue il porting del codice IRIS GL, impostare questo componente alfa su 1,0, indicando un'opacità del 100%. I valori alfa vengono quindi determinati solo dal componente alfa dei materiali, in modo che gli oggetti nella scena siano uguali a quanto fatto in IRIS GL.

La tabella seguente elenca le funzioni di illuminazione e materiali IRIS GL e le relative funzioni OpenGL equivalenti.



| Funzione GL IRIS                 | Funzione OpenGL                               | Significato                                                       |
|----------------------------------|-----------------------------------------------|---------------------------------------------------------------|
| **Imdef(DEFLIGHT,**... **)**    | [glLight](gllight-functions.md)              | Definire una sorgente di luce.                                        |
| **Imdef(DEFLMODEL**, ... **)**   | [glLightModel](gllightmodel-functions.md)    | Definire un modello di illuminazione.                                      |
| **Ambiente di imbind**                       | [**glEnable**](glenable.md) ( GL \_ LIGHT *i*) | Abilitare light *i*.                                             |
| **Ambiente di imbind**                       | **glEnable**( GL \_ LIGHTING )                  | Abilitare l'illuminazione.                                              |
| **Imdef(DEFMATERIAL,**... **)** | [**glMaterial**](glmaterial-functions.md)    | Definire un materiale.                                            |
| **Imcolor**                      | [**glColorMaterial**](glcolormaterial.md)    | Modificare l'effetto dei comandi di colore mentre l'illuminazione è attiva. |
|                                  | [**glGetMaterial**](glgetmaterial.md)        | Ottenere i parametri del materiale.                                      |



 

Nella tabella seguente sono elencati vari parametri di materiale IRIS GL e i relativi parametri OpenGL equivalenti.



| Indice Imdef  | Parametro glMaterial                              | Predefinito              | Significato                                                                                       |
|--------------|---------------------------------------------------|----------------------|-----------------------------------------------------------------------------------------------|
| Alfa        | GL \_ DIFFUSE                                       |                      | Il quarto valore nel parametro GL \_ DIFFUSE specifica il valore alfa.                      |
| Ambientale      | AMBIENTE \_ GL                                       | (0.2, 0.2, 0.2, 1.0) | Colore ambiente.                                                                                |
| Diffusa      | GL \_ DIFFUSE                                       | (0.8, 0.8, 0.8, 1.0) | Colore diffuso.                                                                                |
| Speculare     | \_SPECULARE GL                                      | (0.0, 0.0, 0.0, 1.0) | Colore emissivo.                                                                               |
| LUMINOSITÀ    | GL \_ SHININESSGL \_ AMBIENTE E \_ \_ DIFFUSIONE<br/> | 0,0                  | Esponente speculare. Equivale a chiamare **glMaterial** due volte con gli stessi valori.<br/> |
| COLORINDEXES | INDICI \_ DEI \_ COLORI GL                                |                      | Indici dei colori per l'illuminazione ambiente, diffusa e speculare.                                    |



 

Quando il primo parametro di **Imdef** è DEFMODEL, la traduzione OpenGL equivalente è la funzione [**glLightModel**](gllightmodel-functions.md). L'eccezione si verifica quando il parametro defMODEL seguente è ATTENUATION: la funzione OpenGL equivalente è [**glLight**](gllight-functions.md).

Nella tabella seguente sono elencati i parametri equivalenti del modello di illuminazione per IRIS GL e OpenGL.



| Indice Imdef | Parametro glLightModel          | Predefinito              | Significato                                          |
|-------------|---------------------------------|----------------------|--------------------------------------------------|
| Ambientale     | AMBIENTE DEL MODELLO GL \_ LIGHT \_ \_       | (0.2, 0.2, 0.2, 1.0) | Colore ambientale della scena.                          |
| Attenuazione |                                 |                      | Vedere [**glLight**](gllight-functions.md).        |
| LOCALVIEWER | VISUALIZZATORE \_ LOCALE \_ DEL \_ MODELLO \_ GL LIGHT | GL \_ FALSE            | Visualizzatore locale (**TRUE**) o infinito (**FALSE**). |
| TWOSIDE     | GL \_ LIGHTMODEL \_ DUE \_ LATI       | GL \_ FALSE            | Usare l'illuminazione a due lati quando **TRUE**.            |



 

Quando il primo parametro di **Imdef** è DEFLIGHT, la traduzione OpenGL equivalente è la [**funzione glLight.**](gllight-functions.md)

Nella tabella seguente sono elencati i parametri di illuminazione equivalenti per IRIS GL e OpenGL.



| Indice Imdef           | Parametro glLight                                                                                 | Predefinito                                                                             | Significato                                                                        |
|-----------------------|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| Ambientale               | GL \_ AMBIENTGL \_ DIFFUSE<br/> SPECULARE GL \_<br/>                                         | (0.0, 0.0, 0.0, 1.0) (1.0, 1.0, 1.0, 1.0)<br/> (1.0, 1.0, 1.0, 1.0)<br/> | Intensità ambientale. Intensità diffusa.<br/> Intensità speculare.<br/> |
| LCOLOR                | Nessun equivalente.                                                                                    |                                                                                     |                                                                                |
| POSITION              | POSIZIONE \_ GL                                                                                      | (0.0, 0.0, 1.0, 0.0)                                                                | Posizione della luce.                                                             |
| SPOTDIRECTION         | DIREZIONE DEI SPOT GL \_ \_                                                                               | (0, 0, 1)                                                                           | Direzione dell'in evidenza.                                                        |
| Riflettori             | GL \_ SPOT \_ EXPONENTGL \_ SPOT \_ CUTOFF<br/>                                                     | 0180<br/>                                                                     | Distribuzione dell'intensità. Angolo massimo di diffusione della sorgente di luce.<br/>        |
| DEFMODEL, ATTENUAZIONE | ATTENUAZIONE COSTANTE GL \_ \_ ATTENUAZIONE \_ \_ LINEARE DI GL<br/> ATTENUAZIONE \_ QUADRATICA GL \_<br/> | (1, 0, 0)                                                                           | Fattori di attenuazione.                                                           |



 

 

 





