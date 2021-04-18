---
description: Ottiene l'oggetto ISearchItem se l'URL rappresenta un'origine dati della shell effettiva, nota anche come estensione dello spazio dei nomi della shell.
ms.assetid: 7da6344d-b433-48c3-8f75-7bef0295b9ea
title: 'Metodo ISearchItem:: GetParentFolder'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchItem.GetParentFolder
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4209b319e066d5481c669bcca021684f87532a3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306161"
---
# <a name="isearchitemgetparentfolder-method"></a><span data-ttu-id="5c563-103">Metodo ISearchItem:: GetParentFolder</span><span class="sxs-lookup"><span data-stu-id="5c563-103">ISearchItem::GetParentFolder method</span></span>

<span data-ttu-id="5c563-104">Ottiene l'oggetto [**ISearchItem**](-search-isearchitem.md) se l'URL rappresenta un'origine dati della shell effettiva, nota anche come estensione dello spazio dei nomi della shell.</span><span class="sxs-lookup"><span data-stu-id="5c563-104">Gets the [**ISearchItem**](-search-isearchitem.md) object if the URL represents an actual Shell data source (also known as a Shell namespace extension).</span></span>

## <a name="syntax"></a><span data-ttu-id="5c563-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c563-105">Syntax</span></span>


```C++
HRESULT GetParentFolder(
  [out] ppShellFolder **IShellFolder,
  [out] ppidl         *LPITEMIDLIST
);
```



## <a name="parameters"></a><span data-ttu-id="5c563-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5c563-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c563-107">*IShellFolder* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5c563-107">*IShellFolder* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c563-108">Tipo: **ppShellFolder \* \***</span><span class="sxs-lookup"><span data-stu-id="5c563-108">Type: **ppShellFolder\*\***</span></span>

<span data-ttu-id="5c563-109">Nell'output restituito è contenuto l'indirizzo di un puntatore alla cartella che contiene l'URL corrente.</span><span class="sxs-lookup"><span data-stu-id="5c563-109">On return, contains the address of a pointer to the folder that contains the current URL.</span></span> <span data-ttu-id="5c563-110">L' [interfaccia IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) viene esposta da tutti gli oggetti cartella dello spazio dei nomi della shell e i relativi metodi vengono usati per gestire le cartelle.</span><span class="sxs-lookup"><span data-stu-id="5c563-110">[IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) is exposed by all Shell namespace folder objects, and its methods are used to manage folders.</span></span>

</dd> <dt>

<span data-ttu-id="5c563-111">*LPITEMIDLIST* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5c563-111">*LPITEMIDLIST* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c563-112">Tipo: \**ppidl \** _</span><span class="sxs-lookup"><span data-stu-id="5c563-112">Type: \**ppidl\** _</span></span>

<span data-ttu-id="5c563-113">Nell'output restituito è contenuto l'indirizzo di un puntatore a un elenco di identificatori di elemento (PIDL) che identifica la cartella padre.</span><span class="sxs-lookup"><span data-stu-id="5c563-113">On return, contains the address of a pointer to an item identifier list (PIDL) that identifies the parent folder.</span></span> <span data-ttu-id="5c563-114">Il parametro _LPITEMIDLIST \* può fare riferimento a un oggetto a qualsiasi livello sotto la cartella padre nella gerarchia dello spazio dei nomi e può quindi essere un puntatore a più livelli a un **PIDL** relativo alla cartella padre.</span><span class="sxs-lookup"><span data-stu-id="5c563-114">The _LPITEMIDLIST\* parameter can refer to an object at any level below the parent folder in the namespace hierarchy, and can thus be a multi-level pointer to a **pidl** relative to the parent folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c563-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5c563-115">Return value</span></span>

<span data-ttu-id="5c563-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5c563-116">Type: **HRESULT**</span></span>

<span data-ttu-id="5c563-117">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5c563-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5c563-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5c563-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c563-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c563-119">Remarks</span></span>

<span data-ttu-id="5c563-120">Il metodo **ISearchItem:: GetParentFolder** è supportato solo in Windows XP e windows Server 2003 e non deve più essere usato.</span><span class="sxs-lookup"><span data-stu-id="5c563-120">The **ISearchItem::GetParentFolder** method is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="5c563-121">Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti in computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare l'interfaccia [**ISearchItem**](-search-isearchitem.md) e le API seguenti: le interfacce [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md)e [**ISearchProtocolUI**](-search-isearchprotocolui.md) , la struttura [**LINKINFO**](-search-linkinfo.md) e l'enumerazione [**LinkType**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="5c563-121">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**ISearchItem**](-search-isearchitem.md) interface, and the following APIs: the [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md), and [**ISearchProtocolUI**](-search-isearchprotocolui.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c563-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c563-122">Requirements</span></span>



| <span data-ttu-id="5c563-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c563-123">Requirement</span></span> | <span data-ttu-id="5c563-124">Valore</span><span class="sxs-lookup"><span data-stu-id="5c563-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5c563-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c563-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5c563-126">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5c563-126">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5c563-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c563-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5c563-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5c563-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5c563-129">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="5c563-129">Redistributable</span></span><br/>          | <span data-ttu-id="5c563-130">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="5c563-130">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="5c563-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c563-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c563-132">**ISearchItem**</span><span class="sxs-lookup"><span data-stu-id="5c563-132">**ISearchItem**</span></span>](-search-isearchitem.md)
</dt> </dl>

 

 
