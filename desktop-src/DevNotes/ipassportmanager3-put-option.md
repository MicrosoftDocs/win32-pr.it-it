---
description: Imposta un'opzione di accesso Microsoft .NET Passport specifica.
ms.assetid: 5ec79faa-1c74-42a4-b964-ea15edacda79
title: IPassportManager3::p ut_Option metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPassportManager3.put_Option
api_type:
- COM
api_location: ''
ms.openlocfilehash: 52a1324c4b1a04a207b5bccac1a95bcd060be8ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965928"
---
# <a name="ipassportmanager3put_option-method"></a><span data-ttu-id="55956-103">IPassportManager3: \_ Metodo Option ut:p</span><span class="sxs-lookup"><span data-stu-id="55956-103">IPassportManager3::put\_Option method</span></span>

<span data-ttu-id="55956-104">Imposta un'opzione di accesso Microsoft .NET Passport specifica.</span><span class="sxs-lookup"><span data-stu-id="55956-104">Sets a specific Microsoft .NET Passport sign-in option.</span></span>

> [!Note]  
> <span data-ttu-id="55956-105">Il metodo **put \_ Option** appartiene all'interfaccia [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="55956-105">The **put\_Option** method belongs to the [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) interface.</span></span> <span data-ttu-id="55956-106">Questo argomento integra la documentazione iniziale.</span><span class="sxs-lookup"><span data-stu-id="55956-106">This topic supplements the initial documentation.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="55956-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55956-107">Syntax</span></span>


```C++
HRESULT put_Option(
   BSTR    name,
   VARIANT newVal
);
```



## <a name="parameters"></a><span data-ttu-id="55956-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="55956-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55956-109">*nome*</span><span class="sxs-lookup"><span data-stu-id="55956-109">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="55956-110">Opzione di accesso da impostare.</span><span class="sxs-lookup"><span data-stu-id="55956-110">The sign-in option to be set.</span></span> <span data-ttu-id="55956-111">Attualmente, l'unica opzione supportata è iMode.</span><span class="sxs-lookup"><span data-stu-id="55956-111">Currently, the only supported option is iMode.</span></span>

</dd> <dt>

<span data-ttu-id="55956-112">*newVal*</span><span class="sxs-lookup"><span data-stu-id="55956-112">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="55956-113">**Variant** (VT \_ bool) che specifica il nuovo valore per l'opzione.</span><span class="sxs-lookup"><span data-stu-id="55956-113">A **VARIANT** (VT\_BOOL) that specifies the new value for the option.</span></span> <span data-ttu-id="55956-114">Questo valore può essere true o false.</span><span class="sxs-lookup"><span data-stu-id="55956-114">This value can be True or False.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55956-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="55956-115">Return value</span></span>

<span data-ttu-id="55956-116">Restituisce \_ OK quando il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="55956-116">Returns S\_OK when the method succeeds.</span></span>

## <a name="remarks"></a><span data-ttu-id="55956-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="55956-117">Remarks</span></span>

<span data-ttu-id="55956-118">Questo metodo viene fornito con le versioni precedenti di Passport SDK.</span><span class="sxs-lookup"><span data-stu-id="55956-118">This method ships with older versions of the Passport SDK.</span></span>

 

 
