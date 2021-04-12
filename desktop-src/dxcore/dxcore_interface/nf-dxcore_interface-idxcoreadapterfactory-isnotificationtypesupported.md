---
title: IDXCoreAdapterFactory::IsNotificationTypeSupported
description: Determina se un tipo di notifica specificato è supportato dal sistema operativo.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 78730167e7ec139733ee1e4011d2e5e59c32782b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338583"
---
# <a name="idxcoreadapterfactoryisnotificationtypesupported-method"></a><span data-ttu-id="e93d4-103">Metodo IDXCoreAdapterFactory:: IsNotificationTypeSupported</span><span class="sxs-lookup"><span data-stu-id="e93d4-103">IDXCoreAdapterFactory::IsNotificationTypeSupported method</span></span>

<span data-ttu-id="e93d4-104">Determina se un tipo di notifica specificato è supportato dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e93d4-104">Determines whether a specified notification type is supported by the operating system (OS).</span></span> <span data-ttu-id="e93d4-105">Per istruzioni sulla programmazione ed esempi di codice, vedere [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="e93d4-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e93d4-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e93d4-106">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsNotificationTypeSupported(
  DXCoreNotificationType notificationType) = 0;
```

## <a name="parameters"></a><span data-ttu-id="e93d4-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e93d4-107">Parameters</span></span>

### <a name="notificationtype"></a><span data-ttu-id="e93d4-108">notificationType</span><span class="sxs-lookup"><span data-stu-id="e93d4-108">notificationType</span></span>

<span data-ttu-id="e93d4-109">Tipo: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**</span><span class="sxs-lookup"><span data-stu-id="e93d4-109">Type: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**</span></span>

<span data-ttu-id="e93d4-110">Tipo di notifica di cui si sta eseguendo una query sul supporto per.</span><span class="sxs-lookup"><span data-stu-id="e93d4-110">The type of notification that you're querying about support for.</span></span> <span data-ttu-id="e93d4-111">Per informazioni sui tipi di notifica, vedere la tabella in [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) .</span><span class="sxs-lookup"><span data-stu-id="e93d4-111">See the table in [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) for info about the notification types.</span></span>

## <a name="returns"></a><span data-ttu-id="e93d4-112">Restituisce</span><span class="sxs-lookup"><span data-stu-id="e93d4-112">Returns</span></span>

<span data-ttu-id="e93d4-113">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="e93d4-113">Type: **bool**</span></span>

<span data-ttu-id="e93d4-114">Restituisce  `true`   se il tipo di notifica è supportato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="e93d4-114">Returns `true` if the notification type is supported by the system.</span></span> <span data-ttu-id="e93d4-115">In caso contrario, restituisce  `false` .</span><span class="sxs-lookup"><span data-stu-id="e93d4-115">Otherwise, returns `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="e93d4-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="e93d4-116">Remarks</span></span>

<span data-ttu-id="e93d4-117">È possibile chiamare **IsNotificationTypeSupported** per determinare se un tipo di notifica specificato è noto a questa versione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e93d4-117">You can call **IsNotificationTypeSupported** to determine whether a given notification type is known to this version of the OS.</span></span> <span data-ttu-id="e93d4-118">Ad esempio, un tipo di notifica introdotto in una particolare versione di Windows è sconosciuto alle versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="e93d4-118">For example, a notification type that's introduced in a particular version of Windows is unknown to previous versions of Windows.</span></span>

## <a name="see-also"></a><span data-ttu-id="e93d4-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e93d4-119">See also</span></span>

<span data-ttu-id="e93d4-120">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [riferimento a DXCore](../dxcore-reference.md), [GUID dell'attributo della scheda DXCore](../dxcore-adapter-attribute-guids.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="e93d4-120">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>