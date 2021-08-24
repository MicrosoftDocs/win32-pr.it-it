---
description: Ruota un vettore a sinistra di un determinato numero di componenti a 32 bit e inserisce gli elementi selezionati del risultato in un altro vettore.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorinsert(xmvector,xmvector)
title: Modello XMVectorInsert (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b90eb7348639e6993cb69ef9e82ab78ed989999ea8423f1f6ff8bd9deb7c70d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739752"
---
# <a name="xmvectorinsert-template"></a>Modello XMVectorInsert

Ruota un vettore a sinistra di un determinato numero di componenti a 32 bit e inserisce gli elementi selezionati del risultato in un altro vettore.

## <a name="syntax"></a>Sintassi

``` syntax
template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3> XMVECTOR XMVectorInsert(
  [in]  XMVECTOR VD,
  [in]  XMVECTOR VS
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="VD"></span><span id="vd"></span>*Vd*
</dt> <dd>

\[in \] Vector in cui inserire.

</dd> <dt>

<span id="VS"></span><span id="vs"></span>*Vs*
</dt> <dd>

\[in \] Vector per ruotare a sinistra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce [**l'oggetto XMVECTOR**](xmvector-data-type.md) che risulta dalla rotazione e dall'inserimento.

## <a name="remarks"></a>Commenti

Questa funzione è una versione modello di [**XMVectorInsert**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert) in cui gli *argomenti Select \** sono valori di modello.

Per prestazioni ottimali, il risultato di `XMVectorInsert` deve essere assegnato nuovamente a *VD.*

> [!Note]  
> Il `XMVectorInsert` modello è una novità di DirectXMath e non è disponibile per XNAMath 2.x.

 

**Spazio dei** nomi: usare DirectX

### <a name="platform-requirements"></a>Requisiti della piattaforma

Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con Windows SDK per Windows 8. Supportato per app desktop Win32, app Windows Store e app Windows Phone 8.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>DirectXMath.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni del modello della libreria DirectXMath](ovw-xnamath-templates.md)
</dt> <dt>

[**XMVectorPermute**](xmvectorpermute-template.md)
</dt> <dt>

[**XMVectorRotateLeft**](xmvectorrotateleft-template.md)
</dt> <dt>

[**XMVectorRotateRight**](xmvectorrotateright-template.md)
</dt> <dt>

[**XMVectorShiftLeft**](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
