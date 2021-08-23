---
description: TSPIMessage è un tipo di enumerazione che definisce il set di funzioni LINEEVENT e PHONEEVENT aggiuntive visualizzate in TSPI che non vengono visualizzate in TAPI.
ms.assetid: b3c4ce68-033f-42f1-8c37-66326d21bf32
title: TSPIMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1f74b412d131fc40a13f9da13dc86ba4f31a3becf6bb747e95131bc3bb0e2bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739161"
---
# <a name="tspimessage"></a>TSPIMessage

**TSPIMessage è** un tipo di enumerazione che definisce il set di funzioni [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) e [**PHONEEVENT**](/windows/desktop/api/tspi/nc-tspi-phoneevent) aggiuntive visualizzate in TSPI che non vengono visualizzate in TAPI.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="TSPI_MESSAGE_BASE"></span><span id="tspi_message_base"></span>BASE MESSAGGI \_ \_ TSPI
</dt> <dd>

Numero più basso nell'intervallo di valori di messaggio specifici di TSPI. Questo valore non ha alcun significato da solo, ma funge da base per la definizione degli altri valori.

</dd> <dt>

<span id="LINE_NEWCALL"></span><span id="line_newcall"></span>LINE \_ NEWCALL
</dt> <dd>

Specifica l'arrivo di una nuova chiamata in ingresso che la introduce in TAPI. Deve trattarsi del primo messaggio inviato a TAPI per una nuova chiamata in ingresso. TAPI restituisce il relativo identificatore opaco per la chiamata come parte della gestione di questo messaggio.

</dd> <dt>

<span id="LINE_CALLDEVSPECIFIC"></span><span id="line_calldevspecific"></span>LINE \_ CALLDEVSPECIFIC
</dt> <dd>

Specifica che si è verificato un evento specifico del dispositivo in un dispositivo di chiamata.

</dd> <dt>

<span id="LINE_CALLDEVSPECIFICFEATURE"></span><span id="line_calldevspecificfeature"></span>LINE \_ CALLDEVSPECIFICFEATURE
</dt> <dd>

Specifica che si è verificato un evento di funzionalità specifico del dispositivo in un dispositivo di chiamata.

</dd> </dl>

 

 
