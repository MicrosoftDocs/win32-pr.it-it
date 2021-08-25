---
description: Le enumerazioni seguenti vengono utilizzate nella comunicazione asincrona tra applicazioni e componenti ospitati dallo spooler di stampa, ad esempio i driver della stampante e i monitor di porta.
ms.assetid: 732a552b-caf9-45da-9a9e-a325c4f6341b
title: Enumerazioni di notifica di stampa asincrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a86082d171fbf76afc4a7f02a9511fc7ad3d118ced1aa2ef4f43f87a2abd111
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950731"
---
# <a name="asynchronous-printing-notification-enumerations"></a>Enumerazioni di notifica di stampa asincrona

Le enumerazioni seguenti vengono utilizzate nella comunicazione asincrona tra applicazioni e componenti ospitati dallo spooler di stampa, ad esempio i driver della stampante e i monitor di porta.

## <a name="in-this-section"></a>Contenuto della sezione



| Enumerazione                                                                               | Descrizione                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PrintAsyncNotifyConversationStyle**](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyconversationstyle)<br/> | Specifica se la comunicazione è bidirezionale o unidirezionale tra applicazioni e componenti ospitati da Spooler di stampa, ad esempio driver della stampante, processori di stampa e monitor di porta.<br/>           |
| [**PrintAsyncNotifyError**](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyerror)<br/>                         | Specifica la parte del codice di errore del **valore HRESULT restituita** dopo un errore di notifica asincrona.<br/>                                                                                            |
| [**PrintAsyncNotifyUserFilter**](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyuserfilter)<br/>               | Specifica se le notifiche verranno inviate solo alle applicazioni in ascolto associate allo stesso utente del mittente ospitato dallo Spooler di stampa o a un set più ampio di applicazioni in ascolto.<br/> |



 

 

 




