---
description: Il metodo CollectUserInfo dell'oggetto Installer richiama una sequenza della procedura guidata dell'interfaccia utente che raccoglie e archivia sia le informazioni utente che il codice del prodotto.
ms.assetid: 2faacf38-1af1-4e8a-a3f6-87733104614e
title: Metodo Installer.CollectUserInfo
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
ms.openlocfilehash: 255f9c5bfbd9f7ed476314e8ac1c9ed58568c083b8f6ea7704bbe5cfef15b769
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632918"
---
# <a name="installercollectuserinfo-method"></a>Metodo Installer.CollectUserInfo

Il **metodo CollectUserInfo dell'oggetto** [**Installer**](installer-object.md) richiama una sequenza della procedura guidata dell'interfaccia utente che raccoglie e archivia sia le informazioni utente che il codice del prodotto.

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

Specifica il [**codice prodotto**](productcode.md) del prodotto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Un'applicazione deve chiamare **il metodo CollectUserInfo** la prima volta che viene eseguita. Il **metodo CollectUserInfo** apre il pacchetto di installazione del prodotto e richiama una sequenza di creazione guidata dell'interfaccia utente che raccoglie le informazioni utente. Al termine della sequenza della procedura guidata, le informazioni utente raccolte vengono registrate. La [**proprietà UILevel**](installer-uilevel.md) deve essere impostata su msiUILevelFull perché questa API richiede un'interfaccia utente personalizzata.

Il **metodo CollectUserInfo** richiama [firstRun Dialog.](firstrun-dialog.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa)
</dt> </dl>

 

 




