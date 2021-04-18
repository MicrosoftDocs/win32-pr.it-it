---
description: Funzione creatrice statica che può creare un XamlUIPresenter per una superficie di rendering in un'applicazione desktop.
ms.assetid: 3160E4C2-39D3-8FF5-ED37-78E645D1AC2E
title: CreateXamlUIPresenter (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateXamlUIPresenter
api_type:
- DllExport
api_location:
- Windows.UI.Xaml.dll
ms.openlocfilehash: f9561a179ec4501406e26cb2bbc38ea69b64b979
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333903"
---
# <a name="createxamluipresenter-function"></a>CreateXamlUIPresenter (funzione)

Funzione creatrice statica che può creare un [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) per una superficie di rendering in un'applicazione desktop.

## <a name="syntax"></a>Sintassi


```C++
 static HRESULT WINAPI CreateXamlUIPresenter(
  _In_  IViewObjectPresentNotifySite                 *pPresentSite,
  _Out_ Windows::UI::Xaml::Hosting::IXamlUIPresenter **ppPresenter
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPresentSite* \[ in\]
</dt> <dd>

Interfaccia host esistente. Vedere **IViewObjectPresentNotifySite** nella documentazione di Internet Explorer.

</dd> <dt>

*ppPresenter* \[ out\]
</dt> <dd>

Interfaccia **\[ ExclusiveTo \]** per un [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un **HRESULT** standard, **S \_ OK** per l'esito positivo.

## <a name="remarks"></a>Commenti

Per chiamare questo metodo è necessario un **dllimport** da Windows.UI.Xaml.dll.

Non è possibile chiamare questo metodo da un'app di Windows Store.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Windows. UI. XAML-coretypes. idl</dt> </dl> |
| DLL<br/>    | <dl> <dt>Windows.UI.Xaml.dll</dt> </dl>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041)
</dt> </dl>

 

 
