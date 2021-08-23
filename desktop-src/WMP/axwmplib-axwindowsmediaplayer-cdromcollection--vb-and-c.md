---
title: AxWindowsMediaPlayer.cdromCollection - proprietà
description: La proprietà cdromCollection ottiene un'interfaccia IWMPCdromCollection che fornisce l'accesso a una raccolta di unità CD o DVD.
ms.assetid: 03f4e7d1-4376-4112-993e-943d29aca049
keywords:
- Proprietà cdromCollection Windows Media Player
- Proprietà cdromCollection Windows Media Player , classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player , proprietà cdromCollection
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.cdromCollection
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec885de319153383b82359e35208d19031fa7378749b39033402aba11f8dbd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055017"
---
# <a name="axwindowsmediaplayercdromcollection-property"></a>AxWindowsMediaPlayer.cdromCollection - proprietà

La proprietà cdromCollection ottiene **un'interfaccia IWMPCdromCollection** che fornisce l'accesso a una raccolta di unità CD o DVD.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```CSharp
public IWMPCdromCollection cdromCollection {get;}
```


```VB

Public ReadOnly Property cdromCollection As IWMPCdromCollection
```





## <a name="property-value"></a>Valore proprietà

Interfaccia WMPLib.IWMPCdromCollection.

## <a name="remarks"></a>Commenti

Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                          |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPCdromCollection (VB e C#)**](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





