---
description: Contiene informazioni utilizzate per la creazione di un contesto di Tablet.
ms.assetid: 10466c23-f4cb-4205-886b-d85a2f530afe
title: Struttura TABLET_CONTEXT_SETTINGS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TABLET_CONTEXT_SETTINGS
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9357281409ed4c48b4c6013a7a2be2997d58b094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968607"
---
# <a name="tablet_context_settings-structure"></a><span data-ttu-id="f1bc3-103">\_ \_ Struttura delle impostazioni di contesto del Tablet</span><span class="sxs-lookup"><span data-stu-id="f1bc3-103">TABLET\_CONTEXT\_SETTINGS structure</span></span>

<span data-ttu-id="f1bc3-104">Contiene informazioni utilizzate per la creazione di un contesto di Tablet.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-104">Contains information used in creating a tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1bc3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1bc3-105">Syntax</span></span>


```C++
typedef struct _TABLET_CONTEXT_SETTINGS {
  ULONG cPktProps;
  GUID  *pguidPktProps;
  ULONG cPktBtns;
  GUID  *pguidPktBtns;
  DWORD *pdwBtnDnMask;
  DWORD *pdwBtnUpMask;
  LONG  lXMargin;
  LONG  lYMargin;
} TABLET_CONTEXT_SETTINGS;
```



## <a name="members"></a><span data-ttu-id="f1bc3-106">Members</span><span class="sxs-lookup"><span data-stu-id="f1bc3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f1bc3-107">**cPktProps**</span><span class="sxs-lookup"><span data-stu-id="f1bc3-107">**cPktProps**</span></span>
</dt> <dd>

<span data-ttu-id="f1bc3-108">Numero di proprietà in un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-108">The number of properties in a packet.</span></span>

</dd> <dt>

<span data-ttu-id="f1bc3-109">**pguidPktProps**</span><span class="sxs-lookup"><span data-stu-id="f1bc3-109">**pguidPktProps**</span></span>
</dt> <dd>

<span data-ttu-id="f1bc3-110">Identificatori univoci per le proprietà dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-110">Unique identifiers for the packet properties.</span></span>

</dd> <dt>

<span data-ttu-id="f1bc3-111">**cPktBtns**</span><span class="sxs-lookup"><span data-stu-id="f1bc3-111">**cPktBtns**</span></span>
</dt> <dd>

<span data-ttu-id="f1bc3-112">Numero di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-112">The number of buttons.</span></span>

</dd> <dt>

<span data-ttu-id="f1bc3-113">**pguidPktBtns**</span><span class="sxs-lookup"><span data-stu-id="f1bc3-113">**pguidPktBtns**</span></span>
</dt> <dd>

<span data-ttu-id="f1bc3-114">Identificatori univoci per i pulsanti.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-114">Unique identifiers for the buttons.</span></span>

</dd> <dt>

<span data-ttu-id="f1bc3-115">**pdwBtnDnMask**</span><span class="sxs-lookup"><span data-stu-id="f1bc3-115">**pdwBtnDnMask**</span></span>
</dt> <dd>

<span data-ttu-id="f1bc3-116">Maschera del pulsante verso il basso.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-116">The button down mask.</span></span>

</dd> <dt>

<span data-ttu-id="f1bc3-117">**pdwBtnUpMask**</span><span class="sxs-lookup"><span data-stu-id="f1bc3-117">**pdwBtnUpMask**</span></span>
</dt> <dd>

<span data-ttu-id="f1bc3-118">Maschera del pulsante su.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-118">The button up mask.</span></span>

</dd> <dt>

<span data-ttu-id="f1bc3-119">**lXMargin**</span><span class="sxs-lookup"><span data-stu-id="f1bc3-119">**lXMargin**</span></span>
</dt> <dd>

<span data-ttu-id="f1bc3-120">Margine della direzione X.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-120">The X direction margin.</span></span>

</dd> <dt>

<span data-ttu-id="f1bc3-121">**lYMargin**</span><span class="sxs-lookup"><span data-stu-id="f1bc3-121">**lYMargin**</span></span>
</dt> <dd>

<span data-ttu-id="f1bc3-122">Margine della direzione Y.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-122">The Y direction margin.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1bc3-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="f1bc3-123">Remarks</span></span>

<span data-ttu-id="f1bc3-124">In genere, un'applicazione ottiene i valori predefiniti dal [**Metodo ITablet:: GetDefaultContextSettings**](itablet-getdefaultcontextsettings.md), modifica i valori in base alle proprie esigenze e quindi passa la struttura delle impostazioni modificate al [**Metodo ITablet:: CreateContext**](itablet-createcontext.md).</span><span class="sxs-lookup"><span data-stu-id="f1bc3-124">Typically, an application obtains the default values from the [**ITablet::GetDefaultContextSettings Method**](itablet-getdefaultcontextsettings.md), modifies values to suit their needs, and then passes the modified settings structure to the [**ITablet::CreateContext Method**](itablet-createcontext.md).</span></span>

<span data-ttu-id="f1bc3-125">Questa struttura determina gli eventi che un'applicazione otterrà, il modo in cui verranno elaborati e il modo in cui verranno recapitati all'applicazione o a Windows.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-125">This structure determines what events an application will get, how they will be processed, and how they will be delivered to the application or to Windows itself.</span></span>

<span data-ttu-id="f1bc3-126">Le maschere dei pulsanti stabiliscono insieme i tipi di eventi che verranno elaborati dal contesto.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-126">The button masks together determine what kinds of events will be processed by the context.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1bc3-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1bc3-127">Requirements</span></span>



| <span data-ttu-id="f1bc3-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1bc3-128">Requirement</span></span> | <span data-ttu-id="f1bc3-129">Valore</span><span class="sxs-lookup"><span data-stu-id="f1bc3-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f1bc3-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1bc3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f1bc3-131">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f1bc3-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f1bc3-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1bc3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f1bc3-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f1bc3-133">None supported</span></span><br/>                                     |



 

 




