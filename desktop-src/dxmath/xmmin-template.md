---
description: Confronta due istanze del tipo di dati numerico o due istanze di un oggetto che supporta un overload di < e restituisce quella più piccola delle due istanze. Il tipo di dati degli argomenti e il valore restituito sono uguali.
ms.assetid: m:microsoft.directx_sdk.reference.xmmin(t,t)
title: Modello XMMin (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c2d78b64a66411c31570267c66a7e75171dcf9da039871c07c8bfc31df49149
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118499856"
---
# <a name="xmmin-template"></a>Modello XMMin

Confronta due istanze del tipo di dati numerico o due istanze di un oggetto che supporta un overload di < e restituisce quella più piccola delle due istanze. Il tipo di dati degli argomenti e il valore restituito sono uguali.

## <a name="syntax"></a>Sintassi

``` syntax
template<class T> T XMMin(
  [in]  T a,
  [in]  T b
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="a"></span><span id="A"></span>*Un*
</dt> <dd>

\[in \] specifica il primo di due oggetti .

</dd> <dt>

<span id="b"></span><span id="B"></span>*B*
</dt> <dd>

\[in \] specifica i due di due oggetti .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il più piccolo dei due oggetti di input.

## <a name="remarks"></a>Commenti

`XMMin` è un modello e il tipo T viene specificato quando viene creata un'istanza del modello.

> [!Note]  
> Il `XMMin` modello è una novità di DirectXMath e non è disponibile per XNAMath 2.x. `XMMin` è disponibile come macro in XNAMath 2.x.

 

> [!Note]  
> Usare idealmente std::min invece di `XMMin` . Per evitare conflitti con Windows con std::min, è necessario definire NOMINMAX prima di includere Windows \# intestazioni.

 

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

[**XMMax**](xmmax-template.md)
</dt> </dl>

 

 




