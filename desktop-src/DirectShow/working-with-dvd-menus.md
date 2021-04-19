---
description: Uso dei menu DVD
ms.assetid: 8c5f8072-b74f-4e15-8991-73bcc4145fd2
title: Uso dei menu DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 113647a37200762b5eaf0a9ac231dea74ad19925
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106320048"
---
# <a name="working-with-dvd-menus"></a>Uso dei menu DVD

Il navigatore DVD potrebbe visualizzare un menu quando l'utente attiva un pulsante o quando lo strumento di navigazione entra nel primo dominio di riproduzione. Per visualizzare un menu a livello di codice, chiamare il metodo [**IDVDControl2:: ShowMenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu) .

Sono disponibili diversi modi per selezionare i pulsanti di menu a livello di codice:

-   Per selezionare un pulsante in base al numero, chiamare [**IDVDControl2:: SelectButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton). I pulsanti sono numerati da 1 a 36. Il metodo [**IDvdInfo2:: GetCurrentButton**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentbutton) restituisce il numero di pulsanti disponibili.
-   Per selezionare un pulsante relativo alla posizione del pulsante attualmente selezionato, chiamare [**IDVDControl2:: SelectRelativeButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectrelativebutton). È possibile selezionare un pulsante nella direzione verso l'alto, verso il basso, verso sinistra o verso destra.
-   Per selezionare un pulsante in base alle coordinate all'interno della finestra, chiamare [**IDVDControl2:: SelectAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectatposition). Questo metodo accetta le coordinate (x, y) relative all'area client della finestra del video. Per la modalità senza finestra, si tratta della finestra dell'applicazione. Se non è presente alcun pulsante in tale posizione, il metodo restituisce \_ il \_ pulsante VFW E DVD \_ No \_ .

Sono inoltre disponibili diversi modi per attivare un pulsante:

-   Per attivare un pulsante in base al numero, chiamare [**IDVDControl2:: SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton).
-   Per attivare un pulsante in base alle coordinate, chiamare [**IDVDControl2:: ActivateAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activateatposition).
-   Per attivare il pulsante attualmente selezionato, chiamare [**IDVDControl2:: ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton). Se non è selezionato alcun pulsante, il metodo restituisce \_ il \_ pulsante VFW E DVD \_ No \_ .

Tenere presente che la selezione di un pulsante evidenzia semplicemente i bordi. Per far sì che il comando associato venga attivato, è necessario attivare il pulsante. L'attivazione di un pulsante a livello di codice può essere eseguita in vari modi, ma il pulsante deve sempre essere selezionato prima di poter essere attivato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> </dl>

 

 



