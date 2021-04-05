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
# <a name="tspimessage"></a><span data-ttu-id="0fb18-103">TSPIMessage</span><span class="sxs-lookup"><span data-stu-id="0fb18-103">TSPIMessage</span></span>

<span data-ttu-id="0fb18-104">**TSPIMessage** è un tipo di enumerazione che definisce il set di funzioni [**LineEvent**](/windows/win32/api/tspi/nc-tspi-lineevent) e [**PHONEEVENT**](/windows/desktop/api/tspi/nc-tspi-phoneevent) aggiuntive visualizzate in TSPI che non sono presenti in TAPI.</span><span class="sxs-lookup"><span data-stu-id="0fb18-104">**TSPIMessage** is an enumeration type that defines the set of additional [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) and [**PHONEEVENT**](/windows/desktop/api/tspi/nc-tspi-phoneevent) functions appearing in TSPI that do not appear in TAPI.</span></span>

## <a name="parameters"></a><span data-ttu-id="0fb18-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="0fb18-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fb18-106"><span id="TSPI_MESSAGE_BASE"></span><span id="tspi_message_base"></span>\_base messaggi \_ TSPI</span><span class="sxs-lookup"><span data-stu-id="0fb18-106"><span id="TSPI_MESSAGE_BASE"></span><span id="tspi_message_base"></span>TSPI\_MESSAGE\_BASE</span></span>
</dt> <dd>

<span data-ttu-id="0fb18-107">Il numero più basso nell'intervallo di valori del messaggio specifico di TSPI.</span><span class="sxs-lookup"><span data-stu-id="0fb18-107">The lowest number in the range of TSPI-specific message values.</span></span> <span data-ttu-id="0fb18-108">Questo valore non ha alcun significato da solo, ma funge da base per la definizione degli altri valori.</span><span class="sxs-lookup"><span data-stu-id="0fb18-108">This value has no meaning by itself, but serves as a base for defining the other values.</span></span>

</dd> <dt>

<span data-ttu-id="0fb18-109"><span id="LINE_NEWCALL"></span><span id="line_newcall"></span>LINEA \_ NEWCALL</span><span class="sxs-lookup"><span data-stu-id="0fb18-109"><span id="LINE_NEWCALL"></span><span id="line_newcall"></span>LINE\_NEWCALL</span></span>
</dt> <dd>

<span data-ttu-id="0fb18-110">Specifica che è arrivata una nuova chiamata in ingresso che viene introdotta in TAPI.</span><span class="sxs-lookup"><span data-stu-id="0fb18-110">Specifies that a new, incoming call has arrived and introduces it to TAPI.</span></span> <span data-ttu-id="0fb18-111">Deve essere il primo messaggio inviato a TAPI per una nuova chiamata in ingresso.</span><span class="sxs-lookup"><span data-stu-id="0fb18-111">This must be the first message sent to TAPI for a new incoming call.</span></span> <span data-ttu-id="0fb18-112">TAPI restituisce il relativo identificatore opaco per la chiamata come parte della gestione di questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="0fb18-112">TAPI returns its opaque identifier for the call as part of its handling of this message.</span></span>

</dd> <dt>

<span data-ttu-id="0fb18-113"><span id="LINE_CALLDEVSPECIFIC"></span><span id="line_calldevspecific"></span>LINEA \_ CALLDEVSPECIFIC</span><span class="sxs-lookup"><span data-stu-id="0fb18-113"><span id="LINE_CALLDEVSPECIFIC"></span><span id="line_calldevspecific"></span>LINE\_CALLDEVSPECIFIC</span></span>
</dt> <dd>

<span data-ttu-id="0fb18-114">Specifica che si è verificato un evento specifico del dispositivo in un dispositivo di chiamata.</span><span class="sxs-lookup"><span data-stu-id="0fb18-114">Specifies that a device-specific event has occurred on a call device.</span></span>

</dd> <dt>

<span data-ttu-id="0fb18-115"><span id="LINE_CALLDEVSPECIFICFEATURE"></span><span id="line_calldevspecificfeature"></span>LINEA \_ CALLDEVSPECIFICFEATURE</span><span class="sxs-lookup"><span data-stu-id="0fb18-115"><span id="LINE_CALLDEVSPECIFICFEATURE"></span><span id="line_calldevspecificfeature"></span>LINE\_CALLDEVSPECIFICFEATURE</span></span>
</dt> <dd>

<span data-ttu-id="0fb18-116">Specifica che si è verificato un evento di funzionalità specifico del dispositivo in un dispositivo di chiamata.</span><span class="sxs-lookup"><span data-stu-id="0fb18-116">Specifies that a device-specific feature event has occurred on a call device.</span></span>

</dd> </dl>

 

 
