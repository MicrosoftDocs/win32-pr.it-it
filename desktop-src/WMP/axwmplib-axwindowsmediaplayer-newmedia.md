---
title: AxWindowsMediaPlayer. newMedia, metodo
description: Il metodo newMedia restituisce un'interfaccia IWMPMedia per un nuovo elemento multimediale.
ms.assetid: d10a517e-b4da-4f0b-9d51-9d387578d7dd
keywords:
- Metodo newMedia Windows Media Player
- Metodo newMedia Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player, metodo newMedia
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.newMedia
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 093a4e2b8181aac9148686108ad2c5c318a4d0cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329443"
---
# <a name="axwindowsmediaplayernewmedia-method"></a><span data-ttu-id="38f6b-106">AxWindowsMediaPlayer. newMedia, metodo</span><span class="sxs-lookup"><span data-stu-id="38f6b-106">AxWindowsMediaPlayer.newMedia method</span></span>

<span data-ttu-id="38f6b-107">Il metodo newMedia restituisce un'interfaccia IWMPMedia per un nuovo elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="38f6b-107">The newMedia method returns an IWMPMedia interface for a new media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="38f6b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="38f6b-108">Syntax</span></span>


```CSharp
public IWMPMedia newMedia(
  System.String bstrURL
);
```


```VB

Public Function newMedia( _
  ByVal bstrURL As System.String _
) As IWMPMedia
```





## <a name="parameters"></a><span data-ttu-id="38f6b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="38f6b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38f6b-110">*bstrURL*</span><span class="sxs-lookup"><span data-stu-id="38f6b-110">*bstrURL*</span></span> 
</dt> <dd>

<span data-ttu-id="38f6b-111">**System. String** che rappresenta l'URL del file multimediale digitale utilizzato per inizializzare il nuovo elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="38f6b-111">A **System.String** that is the URL of the digital media file that is used to initialize the new media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38f6b-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="38f6b-112">Return value</span></span>

<span data-ttu-id="38f6b-113">Interfaccia WMPLib. IWMPMedia che rappresenta l'elemento multimediale appena creato.</span><span class="sxs-lookup"><span data-stu-id="38f6b-113">A WMPLib.IWMPMedia interface that represents the newly created media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="38f6b-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="38f6b-114">Remarks</span></span>

<span data-ttu-id="38f6b-115">Il parametro *bstrURL* non deve essere una stringa di lunghezza zero ("") o null.</span><span class="sxs-lookup"><span data-stu-id="38f6b-115">The *bstrURL* parameter must not be a zero-length string ("") or null.</span></span>

## <a name="requirements"></a><span data-ttu-id="38f6b-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38f6b-116">Requirements</span></span>



| <span data-ttu-id="38f6b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="38f6b-117">Requirement</span></span> | <span data-ttu-id="38f6b-118">Valore</span><span class="sxs-lookup"><span data-stu-id="38f6b-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38f6b-119">Versione</span><span class="sxs-lookup"><span data-stu-id="38f6b-119">Version</span></span><br/>   | <span data-ttu-id="38f6b-120">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="38f6b-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="38f6b-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="38f6b-121">Namespace</span></span><br/> | <span data-ttu-id="38f6b-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="38f6b-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="38f6b-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="38f6b-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="38f6b-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="38f6b-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38f6b-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="38f6b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38f6b-126">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="38f6b-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="38f6b-127">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="38f6b-127">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





