---
description: Funzione di creazione statica che può creare un XamlUIPresenter per una superficie di rendering in un'app desktop.
ms.assetid: 3160E4C2-39D3-8FF5-ED37-78E645D1AC2E
title: Funzione CreateXamlUIPresenter
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
ms.openlocfilehash: 247d676e3e2c85404f96324b1d78e1cd6ec2ab2159092d9a66717b2653ee5a02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323434"
---
# <a name="createxamluipresenter-function"></a>Funzione CreateXamlUIPresenter

Funzione di creazione statica che può creare un [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) per una superficie di rendering in un'app desktop.

## <a name="syntax"></a>Sintassi


```C++
 static HRESULT WINAPI CreateXamlUIPresenter(
  _In_  IViewObjectPresentNotifySite                 *pPresentSite,
  _Out_ Windows::UI::Xaml::Hosting::IXamlUIPresenter **ppPresenter
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPresentSite* \[ Pollici\]
</dt> <dd>

Interfaccia di hosting esistente. Vedere **IViewObjectPresentNotifySite** nella Internet Explorer documentazione.

</dd> <dt>

*ppPresenter* \[ Cambio\]
</dt> <dd>

Interfaccia **\[ exclusiveto \]** per un [**oggetto XamlUIPresenter.**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

HResult standard, **S \_ OK per** l'esito positivo.

## <a name="remarks"></a>Commenti

Per chiamare questo metodo è necessario **un elemento DllImport** Windows.UI.Xaml.dll.

Non è possibile chiamare questo metodo da un'app Windows Store.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Windows.ui.xaml-coretypes.idl</dt> </dl> |
| DLL<br/>    | <dl> <dt>Windows.UI.Xaml.dll</dt> </dl>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041)
</dt> </dl>

 

 
