---
description: Se il criterio di sistema per computer è impostato su &\# 0034; 1&\# 0034;, il programma di installazione scrive i messaggi di debug comuni nel debugger usando la funzione OutputDebugString.
ms.assetid: 0a9416ca-0535-4595-a4f3-b3ef7c2d3a13
title: Debug
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2615b12bb76f4c4da0677bbeb459fa549f8233e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883006"
---
# <a name="debug"></a><span data-ttu-id="622fb-103">Debug</span><span class="sxs-lookup"><span data-stu-id="622fb-103">Debug</span></span>

<span data-ttu-id="622fb-104">Se questo [criterio di sistema](system-policy.md) per computer è impostato su "1", il programma di installazione scrive i messaggi di debug comuni nel debugger usando la funzione [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) .</span><span class="sxs-lookup"><span data-stu-id="622fb-104">If this per-machine [system policy](system-policy.md) is set to "1", the installer writes common debugging messages to the debugger using the [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) function.</span></span> <span data-ttu-id="622fb-105">Se questo valore è impostato su "2", il programma di installazione scrive tutti i messaggi di debug validi nel debugger usando la funzione [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) .</span><span class="sxs-lookup"><span data-stu-id="622fb-105">If this value is set to "2", the installer writes all valid debugging messages to the debugger using the [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) function.</span></span> <span data-ttu-id="622fb-106">Questo criterio è esclusivamente a scopo di debug e potrebbe non essere supportato nelle versioni future di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="622fb-106">This policy is for debugging purposes only and may not be supported in future versions of Windows Installer.</span></span>

<span data-ttu-id="622fb-107">Windows Installer scrive le righe di comando nel file di log solo se il terzo bit (0x04) è impostato nel valore del criterio di debug.</span><span class="sxs-lookup"><span data-stu-id="622fb-107">Windows Installer only writes command lines into the log file if the third (0x04) bit is set in the value of the Debug policy.</span></span> <span data-ttu-id="622fb-108">Pertanto, per visualizzare le righe di comando nel log, impostare il valore del criterio di debug su 7.</span><span class="sxs-lookup"><span data-stu-id="622fb-108">Therefore, to display command lines in the log, set the Debug policy value to 7.</span></span> <span data-ttu-id="622fb-109">Non vengono visualizzate le proprietà associate a un [controllo di modifica](edit-control.md) con l' [attributo di controllo password](password-control-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="622fb-109">This does not display properties associated with an [Edit Control](edit-control.md) having the [Password Control Attribute](password-control-attribute.md).</span></span> <span data-ttu-id="622fb-110">In questo modo le proprietà impostate nella riga di comando saranno visibili nel log anche se la proprietà è inclusa nella proprietà [**MsiHiddenProperties**](msihiddenproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="622fb-110">This will make properties set on the command line visible in the log even if the property is included in the [**MsiHiddenProperties**](msihiddenproperties.md) property.</span></span> <span data-ttu-id="622fb-111">Per ulteriori informazioni, vedere [impedire che le informazioni riservate vengano scritte nel file di log](preventing-confidential-information-from-being-written-into-the-log-file.md).</span><span class="sxs-lookup"><span data-stu-id="622fb-111">For more information, see [Preventing Confidential Information from Being Written into the Log File](preventing-confidential-information-from-being-written-into-the-log-file.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="622fb-112">Chiave del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="622fb-112">Registry Key</span></span>

<span data-ttu-id="622fb-113">**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="622fb-113">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="622fb-114">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="622fb-114">Data Type</span></span>

<span data-ttu-id="622fb-115">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="622fb-115">**REG\_DWORD**</span></span>

 

 
