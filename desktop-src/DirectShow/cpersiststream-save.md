---
description: Salva i dati del filtro nel flusso specificato.
ms.assetid: f45c8c6e-f0bb-4358-805a-da2669706d34
title: Metodo CPersistStream. Save (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.Save
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c16e4820f846d2d60382fabd6aafe3ad82880193
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328924"
---
# <a name="cpersiststreamsave-method"></a><span data-ttu-id="f1fce-103">Metodo CPersistStream. Save</span><span class="sxs-lookup"><span data-stu-id="f1fce-103">CPersistStream.Save method</span></span>

<span data-ttu-id="f1fce-104">Salva i dati del filtro nel flusso specificato.</span><span class="sxs-lookup"><span data-stu-id="f1fce-104">Saves the filter's data to the given stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1fce-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1fce-105">Syntax</span></span>


```C++
HRESULT Save(
   LPSTREAM pStm,
   BOOL     fClearDirty
);
```



## <a name="parameters"></a><span data-ttu-id="f1fce-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f1fce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1fce-107">*pStm*</span><span class="sxs-lookup"><span data-stu-id="f1fce-107">*pStm*</span></span> 
</dt> <dd>

<span data-ttu-id="f1fce-108">Puntatore al flusso in cui salvare i dati.</span><span class="sxs-lookup"><span data-stu-id="f1fce-108">Pointer to the stream to which data is to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="f1fce-109">*fClearDirty*</span><span class="sxs-lookup"><span data-stu-id="f1fce-109">*fClearDirty*</span></span> 
</dt> <dd>

<span data-ttu-id="f1fce-110">Flag che indica se reimpostare il flag Dirty del flusso corrente; **True** indica di reimpostarlo.</span><span class="sxs-lookup"><span data-stu-id="f1fce-110">Flag that indicates whether to reset the current stream's dirty flag; **TRUE** means to reset it.</span></span> <span data-ttu-id="f1fce-111">Quando il metodo viene chiamato come parte di un'operazione di salvataggio, il valore è in genere **true**; quando viene chiamato come parte di un'operazione Save As, il valore è in genere **false**.</span><span class="sxs-lookup"><span data-stu-id="f1fce-111">(When the method is called as part of a Save operation, the value is typically **TRUE**; when called as part of a Save As operation, the value is typically **FALSE**.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1fce-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f1fce-112">Return value</span></span>

<span data-ttu-id="f1fce-113">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f1fce-113">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1fce-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f1fce-114">Remarks</span></span>

<span data-ttu-id="f1fce-115">Questa funzione membro implementa il metodo **IPersistStream:: Save** .</span><span class="sxs-lookup"><span data-stu-id="f1fce-115">This member function implements the **IPersistStream::Save** method.</span></span> <span data-ttu-id="f1fce-116">Chiama **WriteInt** con la versione del software, chiama [**CPersistStream:: WriteToStream**](cpersiststream-writetostream.md) con il flusso in *pstm* e Reimposta **mPS \_ fDirty**.</span><span class="sxs-lookup"><span data-stu-id="f1fce-116">It calls **WriteInt** with the software version, calls [**CPersistStream::WriteToStream**](cpersiststream-writetostream.md) with the stream in *pStm*, and resets **mPS\_fDirty**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1fce-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1fce-117">Requirements</span></span>



| <span data-ttu-id="f1fce-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1fce-118">Requirement</span></span> | <span data-ttu-id="f1fce-119">Valore</span><span class="sxs-lookup"><span data-stu-id="f1fce-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1fce-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f1fce-120">Header</span></span><br/>  | <dl> <span data-ttu-id="f1fce-121"><dt>PStream. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1fce-121"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f1fce-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="f1fce-122">Library</span></span><br/> | <dl> <span data-ttu-id="f1fce-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f1fce-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1fce-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1fce-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1fce-125">**Classe CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="f1fce-125">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




