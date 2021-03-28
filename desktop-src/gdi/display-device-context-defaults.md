---
description: Alla prima creazione di un contesto di dispositivo di visualizzazione, il sistema assegna i valori predefiniti per gli attributi (ovvero, disegnando oggetti, colori e modalità) che comprendono il contesto di dispositivo.
ms.assetid: 1a9244e6-2773-435a-8569-806df3a0cd39
title: Visualizzare le impostazioni predefinite del contesto di dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8abcf79339d4f1cc158253d46cc3eb02ec41311
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880302"
---
# <a name="display-device-context-defaults"></a>Visualizzare le impostazioni predefinite del contesto di dispositivo

Alla prima creazione di un contesto di dispositivo di visualizzazione, il sistema assegna i valori predefiniti per gli attributi (ovvero, disegnando oggetti, colori e modalità) che comprendono il contesto di dispositivo. La tabella seguente mostra i valori predefiniti per gli attributi di un contesto di dispositivo di visualizzazione.



| Attributo                             | Valore predefinito                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Colore di sfondo                      | Impostazione del colore di sfondo dal pannello di controllo, in genere bianco.                                                                               |
| Modalità background                       | OPACO                                                                                                                                        |
| Bitmap                                | nessuno                                                                                                                                          |
| Brush                                 | \_pennello bianco                                                                                                                                  |
| Origine pennello                          | (0, 0)                                                                                                                                         |
| Area di visualizzazione                       | Intera finestra o area client con l'area di aggiornamento ritagliata, in base alle esigenze. È possibile ritagliare anche le finestre figlio e popup nell'area client. |
| Tavolozza                               | \_tavolozza predefinita                                                                                                                              |
| Posizione corrente della penna                  | (0, 0)                                                                                                                                         |
| Origine dispositivo                         | Angolo superiore sinistro della finestra o dell'area client.                                                                                           |
| Modalità di disegno                          | \_COPYPEN R2                                                                                                                                   |
| Carattere                                  | tipo di carattere del sistema \_                                                                                                                                  |
| Spaziatura tra caratteri                | 0                                                                                                                                             |
| Modalità di mapping                          | \_testo mm                                                                                                                                      |
| Penna                                   | \_penna nera                                                                                                                                    |
| Modalità riempimento [**poligono**](/windows/desktop/api/Wingdi/nf-wingdi-polygon) | ALTERNATIVO                                                                                                                                     |
| Modalità Stretch                          | BLACKONWHITE                                                                                                                                  |
| Colore del testo                            | Impostazione del colore del testo dal pannello di controllo (in genere nero).                                                                                     |
| Extent del viewport                       | (1,1)                                                                                                                                         |
| Origine viewport                       | (0, 0)                                                                                                                                         |
| Extent della finestra                         | (1,1)                                                                                                                                         |
| Origine finestra                         | (0, 0)                                                                                                                                         |



 

Un'applicazione può modificare i valori degli attributi di contesto del dispositivo di visualizzazione usando le funzioni di selezione e di attributo, ad esempio [**SelezionaOggetto**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject), [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)e [**SetTextColor**](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor). Ad esempio, un'applicazione può modificare le unità di misura predefinite nel sistema di coordinate usando **SetMapMode** per modificare la modalità di mapping.

Le modifiche apportate ai valori di attributo di un contesto di dispositivo comune, padre o finestra non sono permanenti. Quando un'applicazione rilascia questi contesti di dispositivo, le selezioni correnti, ad esempio la modalità di mapping e l'area di ridimensionamento, vengono perse quando il contesto viene restituito alla cache. Le modifiche a una classe o a un contesto di dispositivo privato vengono mantenute per un periodo illimitato Per ripristinare i valori predefiniti originali, un'applicazione deve impostare in modo esplicito ogni attributo.

 

 



