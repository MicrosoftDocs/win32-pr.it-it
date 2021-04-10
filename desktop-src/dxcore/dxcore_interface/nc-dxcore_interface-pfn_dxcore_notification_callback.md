---
title: PFN_DXCORE_NOTIFICATION_CALLBACK
description: Funzione di callback, implementata dall'applicazione, che viene chiamata da un oggetto DXCore per gli eventi di notifica.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 01d65f6907c60d6c68b612308b9105d18bbe037f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963335"
---
# <a name="pfn_dxcore_notification_callback-callback"></a><span data-ttu-id="46faf-103">CALLBACK PFN_DXCORE_NOTIFICATION_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="46faf-103">PFN_DXCORE_NOTIFICATION_CALLBACK callback</span></span>

<span data-ttu-id="46faf-104">Funzione di callback, implementata dall'applicazione, che viene chiamata da un oggetto DXCore per gli eventi di notifica.</span><span class="sxs-lookup"><span data-stu-id="46faf-104">A callback function (implemented by your application), which is called by a DXCore object for notification events.</span></span>

## <a name="syntax"></a><span data-ttu-id="46faf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46faf-105">Syntax</span></span>

```cpp
typedef void (STDMETHODCALLTYPE *PFN_DXCORE_NOTIFICATION_CALLBACK)(
  DXCoreNotificationType notificationType,
  _In_ IUnknown *object,
  _In_opt_ void *context);
```

## <a name="parameters"></a><span data-ttu-id="46faf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="46faf-106">Parameters</span></span>

### <a name="notificationtype"></a><span data-ttu-id="46faf-107">notificationType</span><span class="sxs-lookup"><span data-stu-id="46faf-107">notificationType</span></span>

<span data-ttu-id="46faf-108">Tipo: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**</span><span class="sxs-lookup"><span data-stu-id="46faf-108">Type: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**</span></span>

<span data-ttu-id="46faf-109">Tipo di notifica che rappresenta questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="46faf-109">The type of notification representing this invocation.</span></span> <span data-ttu-id="46faf-110">Per informazioni sui tipi validi con i tipi di oggetti, vedere la tabella in [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) .</span><span class="sxs-lookup"><span data-stu-id="46faf-110">See the table in [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) for info about what types are valid with which kinds of objects.</span></span>

### <a name="object"></a><span data-ttu-id="46faf-111">object</span><span class="sxs-lookup"><span data-stu-id="46faf-111">object</span></span>

<span data-ttu-id="46faf-112">Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span><span class="sxs-lookup"><span data-stu-id="46faf-112">Type: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span></span>

<span data-ttu-id="46faf-113">Oggetto [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) o [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) che genera la notifica.</span><span class="sxs-lookup"><span data-stu-id="46faf-113">The [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) or [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) object raising the notification.</span></span>

### <a name="context-in"></a><span data-ttu-id="46faf-114">Context [in]</span><span class="sxs-lookup"><span data-stu-id="46faf-114">context [in]</span></span>

<span data-ttu-id="46faf-115">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="46faf-115">Type: **void\***</span></span>

<span data-ttu-id="46faf-116">Puntatore, che può essere `nullptr` , a un oggetto che contiene informazioni sul contesto.</span><span class="sxs-lookup"><span data-stu-id="46faf-116">A pointer, which may be `nullptr`, to an object containing context info.</span></span>

## <a name="see-also"></a><span data-ttu-id="46faf-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46faf-117">See also</span></span>

<span data-ttu-id="46faf-118">Guida di riferimento a [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore](../dxcore-reference.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="46faf-118">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>