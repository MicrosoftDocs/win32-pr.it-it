---
title: Input del mouse (introduzione a Win32 e C++)
description: Input del mouse
ms.assetid: EB074CB6-2BB3-4593-A843-8EE25CA028BE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71a560baf110892ba1b8f277c55fc124888b62b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300746"
---
# <a name="mouse-input-get-started-with-win32-and-c"></a>Input del mouse (introduzione a Win32 e C++)

Windows supporta i topi con un massimo di cinque pulsanti: Left, Middle e Right, oltre a due pulsanti aggiuntivi denominati XBUTTON1 e XBUTTON2.

![illustrazione che mostra i pulsanti a sinistra (1), a destra (2), a metà (3) e a XButton1 (4).](images/mouse.png)

Per la maggior parte dei topi per Windows sono disponibili almeno i pulsanti sinistro e destro. Il pulsante sinistro del mouse viene usato per puntare, selezionare, trascinare e così via. Il pulsante destro del mouse Visualizza in genere un menu di scelta rapida. Alcuni topi hanno una rotellina di scorrimento posizionata tra i pulsanti sinistro e destro. A seconda del mouse, è possibile che la rotellina di scorrimento sia anche selezionabile, rendendola il pulsante intermedio.

I pulsanti XBUTTON1 e XBUTTON2 si trovano spesso sui lati del mouse, vicino alla base. Questi pulsanti aggiuntivi non sono presenti in tutti i topi. Se presente, i pulsanti XBUTTON1 e XBUTTON2 vengono spesso mappati a una funzione dell'applicazione, ad esempio la navigazione in avanti e indietro in un Web browser.

Gli utenti a sinistra spesso trovano più comodo scambiare le funzioni dei pulsanti sinistro e destro, usando il pulsante destro come puntatore, e il pulsante sinistro per visualizzare il menu di scelta rapida. Per questo motivo, nella documentazione della Guida di Windows vengono usati il pulsante dei termini *primari* e i *pulsanti secondari*, che fanno riferimento alla funzione logica anziché alla posizione fisica. Nell'impostazione predefinita (a destra), il pulsante sinistro è il pulsante primario e quello secondario. Tuttavia, i termini *con il pulsante destro del mouse* e il *clic sinistro* fanno riferimento a azioni logiche. *Facendo clic con* il pulsante destro del mouse si fa clic sul pulsante principale, se il pulsante è fisicamente sul lato destro o sinistro del mouse.

Indipendentemente dal modo in cui l'utente configura il mouse, Windows converte automaticamente i messaggi del mouse in modo che siano coerenti. L'utente può scambiare i pulsanti primari e secondari al centro dell'utilizzo del programma e non influirà sul comportamento del programma.

La documentazione MSDN usa il pulsante a *destra* e il pulsante *sinistro* per indicare il pulsante *primario* e *secondario* . Questa terminologia è coerente con i nomi dei messaggi della finestra per l'input del mouse. È sufficiente ricordare che i pulsanti fisici sinistro e destro potrebbero essere scambiati.

## <a name="next"></a>Prossima

[Risposta ai clic del mouse](mouse-clicks.md)

 

 




