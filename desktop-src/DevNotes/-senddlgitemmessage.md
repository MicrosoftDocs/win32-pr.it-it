---
description: Invia un messaggio al controllo specificato in una finestra di dialogo.
ms.assetid: 7c91e432-662c-4dd0-980c-892ce1092077
title: Funzione _SendDlgItemMessage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SendDlgItemMessage
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: ea5595ecef953d81ee947042e6265178c1feecd6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325677"
---
# <a name="_senddlgitemmessage-function"></a><span data-ttu-id="30a73-103">\_SendDlgItemMessage (funzione)</span><span class="sxs-lookup"><span data-stu-id="30a73-103">\_SendDlgItemMessage function</span></span>

<span data-ttu-id="30a73-104">\[Questa funzione è un wrapper per la funzione **SendDlgItemMessage** .</span><span class="sxs-lookup"><span data-stu-id="30a73-104">\[This function is a wrapper over the **SendDlgItemMessage** function.</span></span> <span data-ttu-id="30a73-105">Questa funzione può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="30a73-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="30a73-106">Le applicazioni devono chiamare direttamente **SendDlgItemMessage** .\]</span><span class="sxs-lookup"><span data-stu-id="30a73-106">Applications should call **SendDlgItemMessage** directly.\]</span></span>

<span data-ttu-id="30a73-107">Invia un messaggio al controllo specificato in una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="30a73-107">Sends a message to the specified control in a dialog box.</span></span> <span data-ttu-id="30a73-108">Vedere [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea).</span><span class="sxs-lookup"><span data-stu-id="30a73-108">See [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea).</span></span>

## <a name="syntax"></a><span data-ttu-id="30a73-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="30a73-109">Syntax</span></span>


```C++
LRESULT _SendDlgItemMessage(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="30a73-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="30a73-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30a73-111">*...*</span><span class="sxs-lookup"><span data-stu-id="30a73-111">*...*</span></span> 
<span data-ttu-id="30a73-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="30a73-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="30a73-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30a73-113">Requirements</span></span>



| <span data-ttu-id="30a73-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="30a73-114">Requirement</span></span> | <span data-ttu-id="30a73-115">Valore</span><span class="sxs-lookup"><span data-stu-id="30a73-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30a73-116">DLL</span><span class="sxs-lookup"><span data-stu-id="30a73-116">DLL</span></span><br/> | <dl> <span data-ttu-id="30a73-117"><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30a73-117"><dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30a73-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30a73-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30a73-119">**SendDlgItemMessage**</span><span class="sxs-lookup"><span data-stu-id="30a73-119">**SendDlgItemMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)
</dt> </dl>

 

 
