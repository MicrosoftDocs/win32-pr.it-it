---
description: TSPIMessage è un tipo di enumerazione che definisce il set di funzioni LINEEVENT e PHONEEVENT aggiuntive visualizzate in TSPI che non sono presenti in TAPI.
ms.assetid: b3c4ce68-033f-42f1-8c37-66326d21bf32
title: TSPIMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ed5f081c367c675c565f64146b2201890b8306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753719"
---
# <a name="tspimessage"></a>TSPIMessage

**TSPIMessage** è un tipo di enumerazione che definisce il set di funzioni [**LineEvent**](/windows/win32/api/tspi/nc-tspi-lineevent) e [**PHONEEVENT**](/windows/desktop/api/tspi/nc-tspi-phoneevent) aggiuntive visualizzate in TSPI che non sono presenti in TAPI.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="TSPI_MESSAGE_BASE"></span><span id="tspi_message_base"></span>\_base messaggi \_ TSPI
</dt> <dd>

Il numero più basso nell'intervallo di valori del messaggio specifico di TSPI. Questo valore non ha alcun significato da solo, ma funge da base per la definizione degli altri valori.

</dd> <dt>

<span id="LINE_NEWCALL"></span><span id="line_newcall"></span>LINEA \_ NEWCALL
</dt> <dd>

Specifica che è arrivata una nuova chiamata in ingresso che viene introdotta in TAPI. Deve essere il primo messaggio inviato a TAPI per una nuova chiamata in ingresso. TAPI restituisce il relativo identificatore opaco per la chiamata come parte della gestione di questo messaggio.

</dd> <dt>

<span id="LINE_CALLDEVSPECIFIC"></span><span id="line_calldevspecific"></span>LINEA \_ CALLDEVSPECIFIC
</dt> <dd>

Specifica che si è verificato un evento specifico del dispositivo in un dispositivo di chiamata.

</dd> <dt>

<span id="LINE_CALLDEVSPECIFICFEATURE"></span><span id="line_calldevspecificfeature"></span>LINEA \_ CALLDEVSPECIFICFEATURE
</dt> <dd>

Specifica che si è verificato un evento di funzionalità specifico del dispositivo in un dispositivo di chiamata.

</dd> </dl>

 

 
