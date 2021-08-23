---
description: Confronta due istanze del tipo di dati numerico o due istanze di un oggetto che supporta un overload di < e restituisce la più grande delle due istanze. Il tipo di dati degli argomenti e il valore restituito sono uguali.
ms.assetid: m:microsoft.directx_sdk.reference.xmmax(t,t)
title: Modello XMMax (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 362f486861400223024da5442c5103722bf35dcf8cba715da1397ad4b54c19b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117971"
---
# <a name="xmmax-template"></a>Modello XMMax

Confronta due istanze del tipo di dati numerico o due istanze di un oggetto che supporta un overload di < e restituisce la più grande delle due istanze. Il tipo di dati degli argomenti e il valore restituito sono uguali.

## <a name="syntax"></a>Sintassi

``` syntax
template<class T> T XMMax(
  [in]  T a,
  [in]  T b
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="a"></span><span id="A"></span>*Un*
</dt> <dd>

\[in \] specifica il primo dei due oggetti.

</dd> <dt>

<span id="b"></span><span id="B"></span>*B*
</dt> <dd>

\[in \] specifica i due di due oggetti .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore più grande dei due oggetti di input.

## <a name="remarks"></a>Commenti

`XMMax` è un modello e il tipo T viene specificato quando viene creata un'istanza del modello.

> [!Note]  
> Il `XMMax` modello è nuovo per DirectXMath e non è disponibile per XNAMath 2.x. `XMMax` è disponibile come macro in XNAMath 2.x.

 

> [!Note]  
> Usare idealmente std::max anziché `XMMax` . Per evitare conflitti con Windows intestazioni con std::max, è necessario definire NOMINMAX prima di includere Windows \# intestazioni.

 

**Spazio dei** nomi: usare DirectX

### <a name="platform-requirements"></a>Requisiti della piattaforma

Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con Windows SDK per Windows 8. Supportato per app desktop Win32, app Windows Store e Windows Phone 8 app.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>DirectXMath.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni del modello della libreria DirectXMath](ovw-xnamath-templates.md)
</dt> <dt>

[**XMMin**](xmmin-template.md)
</dt> </dl>

 

 




