---
description: Confronta due istanze di tipi di dati numerici o due istanze di un oggetto che supporta un overload di < e restituisce il più piccolo tra le due istanze. Il tipo di dati degli argomenti e il valore restituito sono gli stessi.
ms.assetid: m:microsoft.directx_sdk.reference.xmmin(t,t)
title: Modello XMMin (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550fd93c9776ad8547502b50817446e64f9bdd64
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324060"
---
# <a name="xmmin-template"></a>Modello XMMin

Confronta due istanze di tipi di dati numerici o due istanze di un oggetto che supporta un overload di < e restituisce il più piccolo tra le due istanze. Il tipo di dati degli argomenti e il valore restituito sono gli stessi.

## <a name="syntax"></a>Sintassi

``` syntax
template<class T> T XMMin(
  [in]  T a,
  [in]  T b
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="a"></span><span id="A"></span>*un*
</dt> <dd>

\[in \] specifica il primo di due oggetti.

</dd> <dt>

<span id="b"></span><span id="B"></span>*b*
</dt> <dd>

\[in \] specifica i due di due oggetti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il più piccolo dei due oggetti di input.

## <a name="remarks"></a>Commenti

`XMMin` è un modello e il tipo T viene specificato quando viene creata un'istanza del modello.

> [!Note]  
> Il `XMMin` modello è una novità di DirectXMath e non è disponibile per XNAMath 2. x. `XMMin` è disponibile come macro in XNAMath 2. x.

 

> [!Note]  
> Utilizzare idealmente std:: min anziché `XMMin` . Per evitare conflitti con le intestazioni di Windows con std:: min, è necessario \# definire NOMINMAX prima di includere le intestazioni di Windows.

 

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

[**XMMax**](xmmax-template.md)
</dt> </dl>

 

 




