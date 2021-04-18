---
title: Struttura OPAQUECOMMAND
description: La struttura OPAQUECOMMAND contiene i dati per i comandi passati attraverso Windows Media Gestione dispositivi a un dispositivo ma che non devono essere utilizzati da Windows Media Gestione dispositivi.
ms.assetid: 5b39cf07-2816-4615-a754-e3f0c57bf4ce
keywords:
- Struttura OPAQUECOMMAND Windows Media Gestione dispositivi
- struttura di Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- OPAQUECOMMAND
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 672147cb99336f95a1ced88a3cc6b8df977aec74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328415"
---
# <a name="opaquecommand-structure"></a><span data-ttu-id="ea6ee-105">Struttura OPAQUECOMMAND</span><span class="sxs-lookup"><span data-stu-id="ea6ee-105">OPAQUECOMMAND structure</span></span>

<span data-ttu-id="ea6ee-106">La struttura **OPAQUECOMMAND** contiene i dati per i comandi passati attraverso windows media gestione dispositivi a un dispositivo ma che non devono essere utilizzati da windows media gestione dispositivi.</span><span class="sxs-lookup"><span data-stu-id="ea6ee-106">The **OPAQUECOMMAND** structure contains data for commands that are passed through Windows Media Device Manager to a device but are not intended to be acted upon by Windows Media Device Manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea6ee-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ea6ee-107">Syntax</span></span>


```C++
typedef struct OPAQUECOMMAND {
  GUID  guidCommand;
  DWORD dwDataLen;
  BYTE  *pData;
  BYTE  abMAC[20];
} ;
```



## <a name="members"></a><span data-ttu-id="ea6ee-108">Members</span><span class="sxs-lookup"><span data-stu-id="ea6ee-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ea6ee-109">**guidCommand**</span><span class="sxs-lookup"><span data-stu-id="ea6ee-109">**guidCommand**</span></span>
</dt> <dd>

<span data-ttu-id="ea6ee-110">**GUID** che rappresenta il comando richiesto.</span><span class="sxs-lookup"><span data-stu-id="ea6ee-110">**GUID** representing the requested command.</span></span>

</dd> <dt>

<span data-ttu-id="ea6ee-111">**dwDataLen**</span><span class="sxs-lookup"><span data-stu-id="ea6ee-111">**dwDataLen**</span></span>
</dt> <dd>

<span data-ttu-id="ea6ee-112">Lunghezza dei dati a cui punta *pData* , in byte.</span><span class="sxs-lookup"><span data-stu-id="ea6ee-112">Length of the data to which *pData* points, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ea6ee-113">**pData**</span><span class="sxs-lookup"><span data-stu-id="ea6ee-113">**pData**</span></span>
</dt> <dd>

<span data-ttu-id="ea6ee-114">Dati necessari per eseguire il comando e/o i dati restituiti dal comando.</span><span class="sxs-lookup"><span data-stu-id="ea6ee-114">Data required to execute the command, and/or data returned by the command.</span></span>

</dd> <dt>

<span data-ttu-id="ea6ee-115">**abMAC \[ 20\]**</span><span class="sxs-lookup"><span data-stu-id="ea6ee-115">**abMAC\[20\]**</span></span>
</dt> <dd>

<span data-ttu-id="ea6ee-116">Questo codice MAC (Message Authentication Code) deve includere il membro **guidCommand** , i dati a cui punta *pdwDataLen* e i dati a cui si riferiscono i punti di *pData* .</span><span class="sxs-lookup"><span data-stu-id="ea6ee-116">This message authentication code (MAC) should include the **guidCommand** member, the data to which *pdwDataLen* points, and the data to which *pData* points, if any.</span></span> <span data-ttu-id="ea6ee-117">Se *pData* è **null**, non deve essere incluso nel Mac.</span><span class="sxs-lookup"><span data-stu-id="ea6ee-117">If *pData* is **NULL**, it must not be included in the MAC.</span></span> <span data-ttu-id="ea6ee-118">WMDM \_ Mac \_ length è definito come 20.</span><span class="sxs-lookup"><span data-stu-id="ea6ee-118">WMDM\_MAC\_LENGTH is defined as 20.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ea6ee-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea6ee-119">Requirements</span></span>



| <span data-ttu-id="ea6ee-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea6ee-120">Requirement</span></span> | <span data-ttu-id="ea6ee-121">Valore</span><span class="sxs-lookup"><span data-stu-id="ea6ee-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ea6ee-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ea6ee-122">Header</span></span><br/> | <dl> <span data-ttu-id="ea6ee-123"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ea6ee-123"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea6ee-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ea6ee-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea6ee-125">**IMDSPDevice::SendOpaqueCommand**</span><span class="sxs-lookup"><span data-stu-id="ea6ee-125">**IMDSPDevice::SendOpaqueCommand**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-sendopaquecommand)
</dt> <dt>

[<span data-ttu-id="ea6ee-126">**IMDSPStorage::SendOpaqueCommands**</span><span class="sxs-lookup"><span data-stu-id="ea6ee-126">**IMDSPStorage::SendOpaqueCommands**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-sendopaquecommand)
</dt> <dt>

[<span data-ttu-id="ea6ee-127">**IWMDMDevice::SendOpaqueCommand**</span><span class="sxs-lookup"><span data-stu-id="ea6ee-127">**IWMDMDevice::SendOpaqueCommand**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-sendopaquecommand)
</dt> <dt>

[<span data-ttu-id="ea6ee-128">**IWMDMStorage::SendOpaqueCommand**</span><span class="sxs-lookup"><span data-stu-id="ea6ee-128">**IWMDMStorage::SendOpaqueCommand**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-sendopaquecommand)
</dt> <dt>

[<span data-ttu-id="ea6ee-129">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="ea6ee-129">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





