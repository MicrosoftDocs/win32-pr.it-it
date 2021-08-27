---
description: Una finestra di dialogo Annulla conferma che l'utente vuole terminare l'installazione. Si tratta di una finestra di dialogo modale.
ms.assetid: 5dab4315-721e-417d-91e0-b38653a65c23
title: Finestra di dialogo Annulla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ac2f0ba12c442b8b0f4445077497c26649b79714d1a1d77af7b2a82e6c1a3f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105391"
---
# <a name="cancel-dialog"></a>Finestra di dialogo Annulla

Una **finestra di** dialogo Annulla conferma che l'utente vuole terminare l'installazione. Si tratta di una finestra di dialogo modale.

Questo tipo di finestra di dialogo contiene in [genere un controllo Text](text-control.md) e due controlli [PushButton.](pushbutton-control.md) I due pulsanti consentono all'utente di tornare all'ultima finestra di dialogo o confermare la chiusura dell'installazione.

[L'oggetto ControlEvent](enddialog-controlevent.md) di EndDialog è collegato a questi due pulsanti nella [tabella ControlEvent](controlevent-table.md). Il *parametro Return* di EndDialog ControlEvent è collegato a  uno dei pulsanti e fa sì che la finestra di dialogo Annulla venga terminata e lo stato attivo torni alla finestra di dialogo precedente. Il *parametro Exit* è collegato all'altro pulsante e fa in modo che l'interfaccia utente restituisa il controllo al programma di installazione con il codice appropriato che indica che l'utente vuole uscire. Il programma di installazione si arresta e visualizza la [finestra di dialogo UserExit](userexit-dialog.md).

 

 



