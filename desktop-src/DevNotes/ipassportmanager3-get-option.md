---
description: Recupera il valore di un'opzione di accesso Microsoft .NET Passport specifica.
ms.assetid: a38ffed3-a45b-4bac-8101-3e09f34f3891
title: 'Metodo IPassportManager3:: get_Option'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPassportManager3.get_Option
api_type:
- COM
api_location: ''
ms.openlocfilehash: 289daf9ffbaad872115d0abfd7a618a4f7e44c10
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401364"
---
# <a name="ipassportmanager3get_option-method"></a><span data-ttu-id="0a048-103">Metodo dell'opzione IPassportManager3:: Get \_</span><span class="sxs-lookup"><span data-stu-id="0a048-103">IPassportManager3::get\_Option method</span></span>

<span data-ttu-id="0a048-104">Recupera il valore di un'opzione di accesso Microsoft .NET Passport specifica.</span><span class="sxs-lookup"><span data-stu-id="0a048-104">Retrieves the value of a specific Microsoft .NET Passport sign-in option.</span></span>

> [!Note]  
> <span data-ttu-id="0a048-105">Il metodo dell' **\_ opzione Get** appartiene all'interfaccia [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="0a048-105">The **get\_Option** method belongs to the [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) interface.</span></span> <span data-ttu-id="0a048-106">Questo argomento integra la documentazione iniziale.</span><span class="sxs-lookup"><span data-stu-id="0a048-106">This topic supplements the initial documentation.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="0a048-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0a048-107">Syntax</span></span>


```C++
HRESULT get_Option(
  [in]  BSTR    name,
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="0a048-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0a048-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a048-109">*nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0a048-109">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a048-110">Opzione di accesso da recuperare.</span><span class="sxs-lookup"><span data-stu-id="0a048-110">The sign-in option to be retrieved.</span></span> <span data-ttu-id="0a048-111">Attualmente, l'unica opzione supportata è "iMode".</span><span class="sxs-lookup"><span data-stu-id="0a048-111">Currently, the only supported option is "iMode".</span></span>

</dd> <dt>

<span data-ttu-id="0a048-112">*pval* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0a048-112">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a048-113">Puntatore a un oggetto **Variant** (VT \_ bool) che riceve il valore dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="0a048-113">A pointer to a **VARIANT** (VT\_BOOL) that receives the value of the option.</span></span> <span data-ttu-id="0a048-114">Questo valore può essere true o false.</span><span class="sxs-lookup"><span data-stu-id="0a048-114">This value can be True or False.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a048-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0a048-115">Return value</span></span>

<span data-ttu-id="0a048-116">Restituisce \_ OK quando il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0a048-116">Returns S\_OK when the method succeeds.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a048-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="0a048-117">Remarks</span></span>

<span data-ttu-id="0a048-118">Questo metodo viene fornito con le versioni precedenti di Passport SDK.</span><span class="sxs-lookup"><span data-stu-id="0a048-118">This method ships with older versions of the Passport SDK.</span></span>

 

 
