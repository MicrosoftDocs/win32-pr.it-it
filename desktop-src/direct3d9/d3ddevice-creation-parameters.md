---
description: Descrive i parametri di creazione per un dispositivo.
ms.assetid: 7db5ef2b-6894-4113-b726-8b238bb4fb2f
title: Struttura D3DDEVICE_CREATION_PARAMETERS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVICE_CREATION_PARAMETERS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 72b2f35f1666ec2095c6ea8f5d5588dc7fd62f2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354474"
---
# <a name="d3ddevice_creation_parameters-structure"></a><span data-ttu-id="f2cc7-103">Struttura dei parametri di \_ creazione D3DDEVICE \_</span><span class="sxs-lookup"><span data-stu-id="f2cc7-103">D3DDEVICE\_CREATION\_PARAMETERS structure</span></span>

<span data-ttu-id="f2cc7-104">Descrive i parametri di creazione per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f2cc7-104">Describes the creation parameters for a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2cc7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f2cc7-105">Syntax</span></span>


```C++
typedef struct D3DDEVICE_CREATION_PARAMETERS {
  UINT       AdapterOrdinal;
  D3DDEVTYPE DeviceType;
  HWND       hFocusWindow;
  DWORD      BehaviorFlags;
} D3DDEVICE_CREATION_PARAMETERS, *LPD3DDEVICE_CREATION_PARAMETERS;
```



## <a name="members"></a><span data-ttu-id="f2cc7-106">Members</span><span class="sxs-lookup"><span data-stu-id="f2cc7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f2cc7-107">**AdapterOrdinal**</span><span class="sxs-lookup"><span data-stu-id="f2cc7-107">**AdapterOrdinal**</span></span>
</dt> <dd>

<span data-ttu-id="f2cc7-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f2cc7-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f2cc7-109">Numero ordinale che indica la scheda di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="f2cc7-109">Ordinal number that denotes the display adapter.</span></span> <span data-ttu-id="f2cc7-110">\_Il valore predefinito di D3DADAPTER è sempre la scheda di visualizzazione principale.</span><span class="sxs-lookup"><span data-stu-id="f2cc7-110">D3DADAPTER\_DEFAULT is always the primary display adapter.</span></span> <span data-ttu-id="f2cc7-111">Utilizzare questo ordinale come parametro dell'adapter per uno dei metodi [**IDirect3D9**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="f2cc7-111">Use this ordinal as the Adapter parameter for any of the [**IDirect3D9**](/windows/desktop/api) methods.</span></span> <span data-ttu-id="f2cc7-112">Si noti che diverse istanze di oggetti Direct3D 9,0 possono utilizzare ordinali diversi.</span><span class="sxs-lookup"><span data-stu-id="f2cc7-112">Note that different instances of Direct3D 9.0 objects can use different ordinals.</span></span> <span data-ttu-id="f2cc7-113">Gli adapter possono immettere o lasciare un sistema quando gli utenti, ad esempio, aggiungono o rimuovono i monitoraggi da un sistema a più monitor o quando eseguono lo scambio a caldo di un portatile.</span><span class="sxs-lookup"><span data-stu-id="f2cc7-113">Adapters can enter or leave a system when users, for example, add or remove monitors from a multiple-monitor system or when they hot-swap a laptop.</span></span> <span data-ttu-id="f2cc7-114">Usare quindi questo ordinale solo in un'istanza di Direct3D 9,0 nota come valida, ovvero Direct3D 9,0 che ha creato questa interfaccia [**IDirect3DDevice9**](/windows/desktop/api) o Direct3D 9,0 restituito da [**getdirect3d**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdirect3d), come chiamato tramite questa interfaccia **IDirect3DDevice9** .</span><span class="sxs-lookup"><span data-stu-id="f2cc7-114">Consequently, use this ordinal only in a Direct3D 9.0 instance known to be valid, that is, either the Direct3D 9.0 that created this [**IDirect3DDevice9**](/windows/desktop/api) interface or the Direct3D 9.0 returned from [**GetDirect3D**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdirect3d), as called through this **IDirect3DDevice9** interface.</span></span>

</dd> <dt>

<span data-ttu-id="f2cc7-115">**DeviceType**</span><span class="sxs-lookup"><span data-stu-id="f2cc7-115">**DeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="f2cc7-116">Tipo: **[ **D3DDEVTYPE**](./d3ddevtype.md)**</span><span class="sxs-lookup"><span data-stu-id="f2cc7-116">Type: **[**D3DDEVTYPE**](./d3ddevtype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f2cc7-117">Membro del tipo enumerato [**D3DDEVTYPE**](./d3ddevtype.md) .</span><span class="sxs-lookup"><span data-stu-id="f2cc7-117">Member of the [**D3DDEVTYPE**](./d3ddevtype.md) enumerated type.</span></span> <span data-ttu-id="f2cc7-118">Indica la quantità di funzionalità emulata per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f2cc7-118">Denotes the amount of emulated functionality for this device.</span></span> <span data-ttu-id="f2cc7-119">Il valore di questo parametro rispecchia il valore passato alla chiamata [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) che ha creato il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f2cc7-119">The value of this parameter mirrors the value passed to the [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) call that created this device.</span></span>

</dd> <dt>

<span data-ttu-id="f2cc7-120">**hFocusWindow**</span><span class="sxs-lookup"><span data-stu-id="f2cc7-120">**hFocusWindow**</span></span>
</dt> <dd>

<span data-ttu-id="f2cc7-121">Tipo: **[ **HWND**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f2cc7-121">Type: **[**HWND**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f2cc7-122">Handle di finestra a cui appartiene lo stato attivo per questo dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f2cc7-122">Window handle to which focus belongs for this Direct3D device.</span></span> <span data-ttu-id="f2cc7-123">Il valore di questo parametro rispecchia il valore passato alla chiamata [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) che ha creato il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f2cc7-123">The value of this parameter mirrors the value passed to the [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) call that created this device.</span></span>

</dd> <dt>

<span data-ttu-id="f2cc7-124">**BehaviorFlags**</span><span class="sxs-lookup"><span data-stu-id="f2cc7-124">**BehaviorFlags**</span></span>
</dt> <dd>

<span data-ttu-id="f2cc7-125">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f2cc7-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f2cc7-126">Combinazione di una o più costanti [D3DCREATE](d3dcreate.md) che controllano il comportamento globale del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f2cc7-126">A combination of one or more [D3DCREATE](d3dcreate.md) constants that control global behavior of the device.</span></span> <span data-ttu-id="f2cc7-127">Queste costanti rispecchiano le costanti passate a [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) al momento della creazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f2cc7-127">These constants mirror the constants passed to [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) when the device was created.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f2cc7-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2cc7-128">Requirements</span></span>



| <span data-ttu-id="f2cc7-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2cc7-129">Requirement</span></span> | <span data-ttu-id="f2cc7-130">Valore</span><span class="sxs-lookup"><span data-stu-id="f2cc7-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2cc7-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f2cc7-131">Header</span></span><br/> | <dl> <span data-ttu-id="f2cc7-132"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2cc7-132"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2cc7-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f2cc7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2cc7-134">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="f2cc7-134">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="f2cc7-135">**GetCreationParameters**</span><span class="sxs-lookup"><span data-stu-id="f2cc7-135">**GetCreationParameters**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getcreationparameters)
</dt> <dt>

[<span data-ttu-id="f2cc7-136">**CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="f2cc7-136">**CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> </dl>

 

 
