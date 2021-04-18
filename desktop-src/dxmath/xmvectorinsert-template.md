---
description: Ruota un vettore lasciato da un determinato numero di componenti a 32 bit e inserisce gli elementi selezionati di tale risultato in un altro vettore.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorinsert(xmvector,xmvector)
title: Modello XMVectorInsert (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3250ad52ab19a127b110b02ecf71543f44708681
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329182"
---
# <a name="xmvectorinsert-template"></a>Modello XMVectorInsert

Ruota un vettore lasciato da un determinato numero di componenti a 32 bit e inserisce gli elementi selezionati di tale risultato in un altro vettore.

## <a name="syntax"></a>Sintassi

``` syntax
template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3> XMVECTOR XMVectorInsert(
  [in]  XMVECTOR VD,
  [in]  XMVECTOR VS
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="VD"></span><span id="vd"></span>*VD*
</dt> <dd>

\[in \] vector da inserire in.

</dd> <dt>

<span id="VS"></span><span id="vs"></span>*VS*
</dt> <dd>

\[in \] Vector per ruotare verso sinistra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il [**XMVECTOR**](xmvector-data-type.md) risultante dalla rotazione e dall'inserimento.

## <a name="remarks"></a>Commenti

Questa funzione è una versione modello di [**XMVectorInsert**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert) in cui gli argomenti *Select \** sono valori di modello.

Per ottenere prestazioni ottimali, il risultato di `XMVectorInsert` deve essere assegnato nuovamente a *VD*.

> [!Note]  
> Il `XMVectorInsert` modello è una novità di DirectXMath e non è disponibile per XNAMath 2. x.

 

**Spazio dei nomi**: usare DirectX

### <a name="platform-requirements"></a>Requisiti della piattaforma

Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con la Windows SDK per Windows 8. Supportato per le app desktop Win32, le app di Windows Store e le app Windows Phone 8.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>DirectXMath. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni del modello di libreria DirectXMath](ovw-xnamath-templates.md)
</dt> <dt>

[**XMVectorPermute**](xmvectorpermute-template.md)
</dt> <dt>

[**XMVectorRotateLeft**](xmvectorrotateleft-template.md)
</dt> <dt>

[**XMVectorRotateRight**](xmvectorrotateright-template.md)
</dt> <dt>

[**XMVectorShiftLeft**](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
