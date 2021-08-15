---
description: Al momento della creazione di un contesto di dispositivo di visualizzazione, il sistema assegna i valori predefiniti per gli attributi (ovvero oggetti di disegno, colori e modalità) che costituiscono il contesto di dispositivo.
ms.assetid: 1a9244e6-2773-435a-8569-806df3a0cd39
title: Visualizzare le impostazioni predefinite del contesto di dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 366c4ecb861b64d2b69836832259e6820e0f8809e4aa478d074220d133ccec55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117887278"
---
# <a name="display-device-context-defaults"></a>Visualizzare le impostazioni predefinite del contesto di dispositivo

Al momento della creazione di un contesto di dispositivo di visualizzazione, il sistema assegna i valori predefiniti per gli attributi (ovvero oggetti di disegno, colori e modalità) che costituiscono il contesto di dispositivo. La tabella seguente mostra i valori predefiniti per gli attributi di un contesto di dispositivo di visualizzazione.



| Attributo                             | Valore predefinito                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Colore di sfondo                      | Impostazione del colore di sfondo Pannello di controllo (in genere, bianco).                                                                               |
| Modalità in background                       | Opaco                                                                                                                                        |
| Bitmap                                | Nessuno                                                                                                                                          |
| Brush                                 | PENNELLO \_ BIANCO                                                                                                                                  |
| Origine del pennello                          | (0,0)                                                                                                                                         |
| Area di ritaglio                       | Intera finestra o area client con l'area di aggiornamento ritagliata, in base alle esigenze. Anche le finestre figlio e popup nell'area client possono essere ritagliate. |
| Tavolozza                               | RIQUADRO \_ PREDEFINITO                                                                                                                              |
| Posizione corrente della penna                  | (0,0)                                                                                                                                         |
| Origine del dispositivo                         | Angolo superiore sinistro della finestra o dell'area client.                                                                                           |
| Modalità di disegno                          | R2 \_ COPYPEN                                                                                                                                   |
| Carattere                                  | TIPO DI \_ CARATTERE DI SISTEMA                                                                                                                                  |
| Spaziatura intercharacter                | 0                                                                                                                                             |
| Modalità di mapping                          | TESTO \_ MM                                                                                                                                      |
| Penna                                   | PENNA \_ NERA                                                                                                                                    |
| [**Modalità poligono**](/windows/desktop/api/Wingdi/nf-wingdi-polygon) -riempimento | Alternativo                                                                                                                                     |
| Modalità stretch                          | BLACKONWHITE                                                                                                                                  |
| Colore del testo                            | Impostazione del colore del testo Pannello di controllo (in genere, nero).                                                                                     |
| Extent del viewport                       | (1,1)                                                                                                                                         |
| Origine del viewport                       | (0,0)                                                                                                                                         |
| Extent della finestra                         | (1,1)                                                                                                                                         |
| Origine della finestra                         | (0,0)                                                                                                                                         |



 

Un'applicazione può modificare i valori degli attributi del contesto di dispositivo di visualizzazione usando le funzioni di selezione e attributo, ad esempio [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject), [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)e [**SetTextColor**](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor). Ad esempio, un'applicazione può modificare le unità di misura predefinite nel sistema di coordinate usando **SetMapMode** per modificare la modalità di mapping.

Le modifiche ai valori degli attributi di un contesto di dispositivo comune, padre o finestra non sono permanenti. Quando un'applicazione rilascia questi contesti di dispositivo, le selezioni correnti, ad esempio la modalità di mapping e l'area di ritaglio, vengono perse quando il contesto viene restituito alla cache. Le modifiche apportate a una classe o a un contesto di dispositivo privato vengono mantenute per un periodo indefinito. Per ripristinare le impostazioni predefinite originali, un'applicazione deve impostare in modo esplicito ogni attributo.

 

 



