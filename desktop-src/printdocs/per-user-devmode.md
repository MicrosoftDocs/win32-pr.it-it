---
description: Un utente può specificare le impostazioni predefinite del documento per una stampante. Questa operazione è denominata DEVMODE per utente perché influiscono solo sulle impostazioni predefinite per un determinato utente e le informazioni per ogni stampante sono definite in una struttura DEVMODE separata.
ms.assetid: f791f847-c31e-4a06-93cb-49117d8f0cb8
title: Per-User DEVMODE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dee5a79d314e0f9ab89210ba4d2644d2b8ec99c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311815"
---
# <a name="per-user-devmode"></a><span data-ttu-id="3b743-104">Per-User DEVMODE</span><span class="sxs-lookup"><span data-stu-id="3b743-104">Per-User DEVMODE</span></span>

<span data-ttu-id="3b743-105">Un utente può specificare le impostazioni predefinite del documento per una stampante.</span><span class="sxs-lookup"><span data-stu-id="3b743-105">A user can specify the default document settings for a printer.</span></span> <span data-ttu-id="3b743-106">Questa operazione è denominata *DEVMODE per utente* perché influiscono solo sulle impostazioni predefinite per un determinato utente e le informazioni per ogni stampante sono definite in una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) separata.</span><span class="sxs-lookup"><span data-stu-id="3b743-106">This is called the *per-user DEVMODE* because it only affects the defaults for a particular user, and the information for each printer is defined in a separate [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure.</span></span>

<span data-ttu-id="3b743-107">Per impostare la struttura DEVMODE per singolo utente, chiamare [**Seprinter**](setprinter.md) con la [**stampante \_ info \_ 2**](printer-info-2.md) o [**Printer \_ info \_ 9**](printer-info-9.md) .</span><span class="sxs-lookup"><span data-stu-id="3b743-107">To set the per-user DEVMODE, call [**SetPrinter**](setprinter.md) with either the [**PRINTER\_INFO\_2**](printer-info-2.md) or the [**PRINTER\_INFO\_9**](printer-info-9.md) structure.</span></span> <span data-ttu-id="3b743-108">Per reimpostare la struttura DEVMODE per ogni utente sulla [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)globale predefinita, chiamare **seprinter** con la struttura della [**stampante \_ info \_ 8**](printer-info-8.md) .</span><span class="sxs-lookup"><span data-stu-id="3b743-108">To reset the per-user DEVMODE to the global default [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea), call **SetPrinter** with the [**PRINTER\_INFO\_8**](printer-info-8.md) structure.</span></span>

 

 



