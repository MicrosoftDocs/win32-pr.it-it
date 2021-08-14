---
title: Porting di funzioni di illuminazione e materiali
description: Le funzioni OpenGL per l'illuminazione e i materiali sono sostanzialmente diverse dalle funzioni IRIS GL. A differenza di IRIS GL, OpenGL ha funzioni separate per l'impostazione di luci, modelli di luce e materiali.
ms.assetid: de57d041-1ea1-46d0-b584-009608625ea5
keywords:
- Portabilità, illuminazione IRIS GL
- porting da IRIS GL, illuminazione
- porting to OpenGL from IRIS GL,lighting
- Porting OpenGL da IRIS GL, illuminazione
- Portabilità IRIS GL, materiali
- porting from IRIS GL,materials
- porting to OpenGL from IRIS GL,materials
- Portabilità OpenGL da IRIS GL, materiali
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
# <a name="porting-lighting-and-materials-functions"></a>Porting di funzioni di illuminazione e materiali

Le funzioni OpenGL per l'illuminazione e i materiali sono sostanzialmente diverse dalle funzioni IRIS GL. A differenza di IRIS GL, OpenGL ha funzioni separate per l'impostazione di luci, modelli di luce e materiali.

Quando si esegue il porting delle funzioni di illuminazione e materiali, tenere presente quanto segue:

-   OpenGL non include una tabella di definizioni archiviate. È possibile usare gli elenchi di visualizzazione per simulare il meccanismo di def/binding IRIS GL. Per altre informazioni su defs e binds, vedere [Porting Defs, Binds, and Sets](porting-defs--binds--and-sets.md).
-   Con OpenGL, l'attenuazione è associata a ogni sorgente di luce, anziché al modello di illuminazione complessivo.
-   I componenti diffusi e speculari sono separati nelle sorgenti di luce OpenGL.
-   Le sorgenti di luce OpenGL hanno un componente alfa. Quando si esegue la portabilità del codice GL IRIS, impostare questo componente alfa su 1,0, che indica un'opacità del 100%. I valori alfa vengono quindi determinati solo dal componente alfa dei materiali, quindi gli oggetti nella scena avranno lo stesso aspetto di IRIS GL.

La tabella seguente elenca le funzioni di illuminazione e materiali IRIS GL e le funzioni OpenGL equivalenti.



| Funzione GL IRIS                 | Funzione OpenGL                               | Significato                                                       |
|----------------------------------|-----------------------------------------------|---------------------------------------------------------------|
| **Imdef(DEFLIGHT**, ... **)**    | [glLight](gllight-functions.md)              | Definire una sorgente di luce.                                        |
| **Imdef(DEFLMODEL**, ... **)**   | [glLightModel](gllightmodel-functions.md)    | Definire un modello di illuminazione.                                      |
| **Imbind**                       | [**glEnable**](glenable.md) ( GL \_ LIGHT *i*) | Abilitare light *i*.                                             |
| **Imbind**                       | **glEnable**( GL \_ LIGHTING )                  | Abilitare l'illuminazione.                                              |
| **Imdef(DEFMATERIAL**, ... **)** | [**glMaterial**](glmaterial-functions.md)    | Definire un materiale.                                            |
| **Imcolor**                      | [**glColorMaterial**](glcolormaterial.md)    | Modificare l'effetto dei comandi colore mentre l'illuminazione è attiva. |
|                                  | [**glGetMaterial**](glgetmaterial.md)        | Ottiene i parametri del materiale.                                      |



 

La tabella seguente elenca vari parametri di materiale IRIS GL e i relativi parametri OpenGL equivalenti.



| Indice Imdef  | parametro glMaterial                              | Predefinito              | Significato                                                                                       |
|--------------|---------------------------------------------------|----------------------|-----------------------------------------------------------------------------------------------|
| Alfa        | GL \_ DIFFUSE                                       |                      | Il quarto valore nel parametro GL \_ DIFFUSE specifica il valore alfa.                      |
| Ambientale      | AMBIENTE \_ GL                                       | (0.2, 0.2, 0.2, 1.0) | Colore ambiente.                                                                                |
| Diffusa      | GL \_ DIFFUSE                                       | (0.8, 0.8, 0.8, 1.0) | Colore diffuso.                                                                                |
| Speculare     | SPECULARE GL \_                                      | (0.0, 0.0, 0.0, 1.0) | Colore emissivo.                                                                               |
| ISTINENZA    | GL \_ SHININESSGL \_ AMBIENT \_ AND \_ DIFFUSE<br/> | 0,0                  | Esponente speculare. Equivale a chiamare **glMaterial due** volte con gli stessi valori.<br/> |
| COLORINDEXES | INDICI COLORI GL \_ \_                                |                      | Indici di colore per l'illuminazione ambientale, diffusa e speculare.                                    |



 

Quando il primo parametro di **Imdef** è DEFMODEL, la conversione OpenGL equivalente è la funzione [**glLightModel**](gllightmodel-functions.md). L'eccezione si verifica quando il parametro che segue DEFMODEL è ATTENUATION: quindi la funzione OpenGL equivalente [**è glLight**](gllight-functions.md).

La tabella seguente elenca i parametri equivalenti del modello di illuminazione per IRIS GL e OpenGL.



| Indice Imdef | Parametro glLightModel          | Predefinito              | Significato                                          |
|-------------|---------------------------------|----------------------|--------------------------------------------------|
| Ambientale     | AMBIENTE \_ DEL \_ MODELLO \_ GL LIGHT       | (0.2, 0.2, 0.2, 1.0) | Colore ambientale della scena.                          |
| Attenuazione |                                 |                      | Vedere [**glLight.**](gllight-functions.md)        |
| LOCALVIEWER | GL \_ LIGHT \_ MODEL \_ LOCAL \_ VIEWER | GL \_ FALSE            | Visualizzatore locale (**TRUE**) o infinito (**FALSE**). |
| TWOSIDE     | GL \_ LIGHTMODEL \_ DUE \_ LATI       | GL \_ FALSE            | Usare l'illuminazione a due lati quando **è TRUE.**            |



 

Quando il primo parametro di **Imdef** è DEFLIGHT, la conversione OpenGL equivalente è la [**funzione glLight.**](gllight-functions.md)

La tabella seguente elenca i parametri di illuminazione equivalenti per IRIS GL e OpenGL.



| Indice Imdef           | Parametro glLight                                                                                 | Predefinito                                                                             | Significato                                                                        |
|-----------------------|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| Ambientale               | GL \_ AMBIENTGL \_ DIFFUSE<br/> \_SPECULARE GL<br/>                                         | (0.0, 0.0, 0.0, 1.0) (1.0, 1.0, 1.0, 1.0)<br/> (1.0, 1.0, 1.0, 1.0)<br/> | Intensità ambiente. Intensità diffusa.<br/> Intensità speculare.<br/> |
| LCOLOR                | Nessun equivalente.                                                                                    |                                                                                     |                                                                                |
| POSITION              | POSIZIONE \_ DI CONTABILITÀ GENERALE                                                                                      | (0.0, 0.0, 1.0, 0.0)                                                                | Posizione della luce.                                                             |
| SPOTDIRECTION         | DIREZIONE \_ DEL PUNTO \_ GL                                                                               | (0, 0, 1)                                                                           | Direzione dei riflettori.                                                        |
| Riflettori             | GL \_ SPOT \_ EXPONENTGL \_ SPOT \_ CUTOFF<br/>                                                     | 0180<br/>                                                                     | Distribuzione dell'intensità. Angolo massimo di diffusione della sorgente di luce.<br/>        |
| DEFMODEL, ATTENUAZIONE | ATTENUAZIONE COSTANTE GL \_ \_ ATTENUAZIONEGL \_ \_ ATTENUAZIONE LINEARE<br/> \_ATTENUAZIONE \_ QUADRATICA GL<br/> | (1, 0, 0)                                                                           | Fattori di attenuazione.                                                           |



 

 

 





