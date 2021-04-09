---
description: Le tabelle messaggi sono risorse di stringa speciali utilizzate per la visualizzazione dei messaggi di errore. Sono dichiarati in un file di risorse usando l'istruzione di definizione della risorsa MESSAGETABLE. Per accedere alle stringhe di messaggio, usare la funzione FormatMessage.
ms.assetid: db84f190-1d1e-4192-8dba-baaee0a3e3ea
title: Tabelle messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe12b28c9b4f89d9a6d32c398a2e246940bb79a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965943"
---
# <a name="message-tables"></a><span data-ttu-id="57578-105">Tabelle messaggi</span><span class="sxs-lookup"><span data-stu-id="57578-105">Message Tables</span></span>

<span data-ttu-id="57578-106">Le tabelle messaggi sono risorse di stringa speciali utilizzate per la visualizzazione dei messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="57578-106">Message tables are special string resources used when displaying error messages.</span></span> <span data-ttu-id="57578-107">Sono dichiarati in un file di risorse usando l'istruzione di definizione della risorsa [MESSAGETABLE](../menurc/messagetable-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="57578-107">They are declared in a resource file using the [MESSAGETABLE](../menurc/messagetable-resource.md) resource-definition statement.</span></span> <span data-ttu-id="57578-108">Per accedere alle stringhe di messaggio, usare la funzione [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) .</span><span class="sxs-lookup"><span data-stu-id="57578-108">To access the message strings, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function.</span></span>

<span data-ttu-id="57578-109">Il sistema fornisce una tabella dei messaggi per i [codici di errore di sistema](system-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="57578-109">The system provides a message table for the [system error codes](system-error-codes.md).</span></span> <span data-ttu-id="57578-110">Per recuperare la stringa che corrisponde al codice di errore, chiamare [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con il \_ messaggio \_ di formato dal \_ flag di sistema.</span><span class="sxs-lookup"><span data-stu-id="57578-110">To retrieve the string that corresponds to the error code, call [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag.</span></span>

<span data-ttu-id="57578-111">Per fornire una tabella dei messaggi per l'applicazione, seguire le istruzioni riportate in [file di testo dei messaggi](../eventlog/message-text-files.md).</span><span class="sxs-lookup"><span data-stu-id="57578-111">To provide a message table for your application, follow the instructions in [Message Text Files](../eventlog/message-text-files.md).</span></span> <span data-ttu-id="57578-112">Per recuperare le stringhe dalla tabella messaggi, chiamare [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con il \_ messaggio Format \_ dal \_ flag HMODULE.</span><span class="sxs-lookup"><span data-stu-id="57578-112">To retrieve strings from your message table, call [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) with the FORMAT\_MESSAGE\_FROM\_HMODULE flag.</span></span>

 

 
