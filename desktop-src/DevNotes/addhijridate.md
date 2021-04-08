---
description: '\\Pannello di controllo HKCU \\ internazionale.'
ms.assetid: e2925d92-19df-42e5-9893-2820f437d3a5
title: AddHijriDate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a1c4a721af18e0a8994efdd7641581aa01c133
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877453"
---
# <a name="addhijridate"></a>AddHijriDate

**\\Pannello di controllo HKCU \\ internazionale**



| Tipo di dati | Range                      | Valore predefinito |
|-----------|----------------------------|---------------|
| REG \_ SZ   | *Valore di regolazione valido* | (nessuna)        |



 

## <a name="description"></a>Descrizione

Specifica le modifiche alla data nel calendario Hijri.

Il calendario Hijri è un calendario lunare usato nel mondo islamico. I mesi iniziano e terminano in base a un decreto che si basa sull'osservazione della nuova luna. È difficile prevedere accuratamente gli inizi e le terminazioni dei mesi e sono presenti variazioni internazionali, quindi viene apportata una modifica tra zero e due giorni al calendario.

Il valore del registro di sistema **AddHijriDate** archivia questo valore di regolazione come indicato di seguito.



| Valore          | Significato                                                                                                                                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AddHijriDate-2 | Sottrarre due giorni.                                                                                                                                                                                                                    |
| AddHijriDate   | Sottrarre un giorno.                                                                                                                                                                                                                     |
| (vuoto)        | Non è necessaria alcuna regolazione. Se la data non è stata modificata, questa voce non viene visualizzata nel registro di sistema. Se la data è stata modificata e quindi ripristinata al valore originale, questa voce viene visualizzata nel registro di sistema senza alcun valore. |
| AddHijriDate + 1 | Aggiungere un giorno.                                                                                                                                                                                                                          |
| AddHijriDate + 2 | Aggiungere due giorni.                                                                                                                                                                                                                         |



 

Questa voce non è disponibile nel Registro di sistema per impostazione predefinita. È possibile aggiungerlo utilizzando l'editor del registro di sistema Regedit.exe o utilizzando il metodo di modifica descritto di seguito.

## <a name="change-method"></a>Cambia metodo

Per modificare il valore di questa voce o per aggiungerlo al registro di sistema, installare prima i file per le lingue con alfabeti non latini e con scrittura da destra a sinistra. Nel pannello di controllo fare clic su **Opzioni internazionali e della lingua**, quindi fare clic sulla scheda **lingue** . In **supporto lingua supplementare** selezionare la casella di controllo per **installare i file per le lingue con alfabeti non latini e da destra a sinistra (incluso Thai)**. Fare clic su **OK**.

Per modificare il valore di questa voce o per aggiungerlo al registro di sistema, nel pannello di controllo fare clic su **Opzioni internazionali e della lingua**. Nel campo **standard e formati** selezionare le impostazioni locali che utilizzano il calendario Hijri. Fare clic sul pulsante **Personalizza** , quindi sulla scheda **Data** . Nell'elenco a discesa **Adjust date Hijri to:** selezionare il valore appropriato. Fare clic su **OK**, quindi fare di nuovo clic su **OK** .

## <a name="activation-method"></a>Metodo di attivazione

Le modifiche apportate a questa voce tramite il pannello di controllo hanno effetto immediato.

 

 



