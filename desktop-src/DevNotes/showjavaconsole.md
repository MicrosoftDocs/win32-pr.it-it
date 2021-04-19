---
description: La funzione ShowJavaConsole è un supporto per il debug di sviluppatori Java. Gli applet (o altro codice Java) in esecuzione in Internet Explorer possono utilizzarlo per visualizzare i messaggi di errore e altre informazioni.
ms.assetid: 070dd833-f8cc-403e-afbf-325648760d5f
title: ShowJavaConsole (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- extern
api_type:
- DllExport
api_location:
- Msjava.dll
ms.openlocfilehash: 522885bfdd07843549375977630d8d1a7c6776f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328176"
---
# <a name="showjavaconsole-function"></a><span data-ttu-id="2728e-104">ShowJavaConsole (funzione)</span><span class="sxs-lookup"><span data-stu-id="2728e-104">ShowJavaConsole function</span></span>

<span data-ttu-id="2728e-105">La funzione **ShowJavaConsole** è un supporto per il debug di sviluppatori Java.</span><span class="sxs-lookup"><span data-stu-id="2728e-105">The **ShowJavaConsole** function is a debugging aid for Java developers.</span></span> <span data-ttu-id="2728e-106">Gli applet (o altro codice Java) in esecuzione in Internet Explorer possono utilizzarlo per visualizzare i messaggi di errore e altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="2728e-106">Applets (or other Java code) running within Internet Explorer can use it to display error messages and other information.</span></span>

## <a name="syntax"></a><span data-ttu-id="2728e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2728e-107">Syntax</span></span>


```C++
void extern ShowJavaConsole(void);
```



## <a name="parameters"></a><span data-ttu-id="2728e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2728e-108">Parameters</span></span>

<span data-ttu-id="2728e-109">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="2728e-109">This function has no parameters.</span></span>

<dl></dl>

## <a name="return-value"></a><span data-ttu-id="2728e-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2728e-110">Return value</span></span>

<span data-ttu-id="2728e-111">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="2728e-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2728e-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="2728e-112">Remarks</span></span>

<span data-ttu-id="2728e-113">La chiamata di **ShowJavaConsole** fa sì che la macchina virtuale Java (VM) visualizzi la finestra della console Java.</span><span class="sxs-lookup"><span data-stu-id="2728e-113">Calling **ShowJavaConsole** causes the Java virtual machine (VM) to display the Java console window.</span></span> <span data-ttu-id="2728e-114">La finestra della console Java può visualizzare l'output del debug dal codice Java in esecuzione nel processo chiamante.</span><span class="sxs-lookup"><span data-stu-id="2728e-114">The Java console window itself can display debugging output from Java code running in the calling process.</span></span> <span data-ttu-id="2728e-115">Questa operazione viene in genere usata solo da un'applicazione che ospita la macchina virtuale Java.</span><span class="sxs-lookup"><span data-stu-id="2728e-115">Typically, this would be used only by an application hosting the Java VM.</span></span> <span data-ttu-id="2728e-116">Esiste una sola finestra della console Java per ogni processo; per più chiamate all'API si ottiene la visualizzazione della stessa finestra.</span><span class="sxs-lookup"><span data-stu-id="2728e-116">There is only a single Java console window per process; multiple calls to the API result in the same window being displayed.</span></span> <span data-ttu-id="2728e-117">In altre parole, se la finestra della console è già visualizzata, non viene eseguita alcuna operazione; Se la finestra non è stata visualizzata o l'utente lo ha chiuso, viene visualizzata la finestra.</span><span class="sxs-lookup"><span data-stu-id="2728e-117">In other words, if the console window is already displayed, nothing happens; if the window has not been displayed, or the user has closed it, then the window pops up.</span></span>

<span data-ttu-id="2728e-118">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="2728e-118">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="2728e-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2728e-119">Requirements</span></span>



| <span data-ttu-id="2728e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2728e-120">Requirement</span></span> | <span data-ttu-id="2728e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="2728e-121">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2728e-122">DLL</span><span class="sxs-lookup"><span data-stu-id="2728e-122">DLL</span></span><br/> | <dl> <span data-ttu-id="2728e-123"><dt>Msjava.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2728e-123"><dt>Msjava.dll</dt></span></span> </dl> |



 

 
