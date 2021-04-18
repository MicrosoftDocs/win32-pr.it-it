---
title: Proprietà AxWindowsMediaPlayer. cdromCollection
description: La proprietà cdromcollection ottiene un'interfaccia IWMPCdromCollection che consente di accedere a una raccolta di unità CD o DVD.
ms.assetid: 03f4e7d1-4376-4112-993e-943d29aca049
keywords:
- Finestra delle proprietà di cdromcollection Media Player
- Proprietà di cdromcollection Media Player di Windows, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player, proprietà cdromcollection
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
ms.openlocfilehash: ac4ba3bb5df95e9ee53e2a6c3aecbd1e9a355882
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323923"
---
# <a name="axwindowsmediaplayercdromcollection-property"></a>Proprietà AxWindowsMediaPlayer. cdromCollection

La proprietà cdromcollection ottiene un'interfaccia **IWMPCdromCollection** che consente di accedere a una raccolta di unità CD o DVD.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```CSharp
public IWMPCdromCollection cdromCollection {get;}
```


```VB

Public ReadOnly Property cdromCollection As IWMPCdromCollection
```





## <a name="property-value"></a>Valore proprietà

Interfaccia WMPLib. IWMPCdromCollection.

## <a name="remarks"></a>Commenti

Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                          |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPCdromCollection (VB e C#)**](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





