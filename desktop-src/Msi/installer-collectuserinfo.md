---
description: Il metodo CollectUserInfo dell'oggetto Installer richiama una sequenza guidata dell'interfaccia utente che raccoglie e archivia sia le informazioni utente sia il codice del prodotto.
ms.assetid: 2faacf38-1af1-4e8a-a3f6-87733104614e
title: Installer. CollectUserInfo, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CollectUserInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d7286fdbc9fab6b3db6752284bf86db05f920bd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329029"
---
# <a name="installercollectuserinfo-method"></a>Installer. CollectUserInfo, metodo

Il metodo **CollectUserInfo** dell'oggetto [**Installer**](installer-object.md) richiama una sequenza guidata dell'interfaccia utente che raccoglie e archivia sia le informazioni utente sia il codice del prodotto.

## <a name="syntax"></a>Sintassi


```JScript
Installer.CollectUserInfo(
  Product
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Prodotto* 
</dt> <dd>

Specifica il [**codice**](productcode.md) del prodotto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Quando viene eseguita la prima volta, un'applicazione deve chiamare il metodo **CollectUserInfo** . Il metodo **CollectUserInfo** apre il pacchetto di installazione del prodotto e richiama una sequenza guidata dell'interfaccia utente creata che raccoglie le informazioni utente. Al termine della sequenza della procedura guidata, le informazioni sull'utente raccolte vengono registrate. La proprietà [**UILevel**](installer-uilevel.md) deve essere impostata su msiUILevelFull perché questa API richiede un'interfaccia utente creata.

Il metodo **CollectUserInfo** richiama la [finestra di dialogo firstrun](firstrun-dialog.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa)
</dt> </dl>

 

 




