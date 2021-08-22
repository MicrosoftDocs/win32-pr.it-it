---
description: Il metodo ForceSourceListResolution dell'oggetto Installer forza Windows Installer di cercare un'origine del prodotto valida nell'elenco di origine.
ms.assetid: d5097331-8cf5-494f-9e88-bcffcad3fe5d
title: Metodo Installer.ForceSourceListResolution
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ForceSourceListResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cafff03a392fc1977fd19b5b8415ca499d614c2c4ba3fb4f7104edd5344f3a86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630593"
---
# <a name="installerforcesourcelistresolution-method"></a>Metodo Installer.ForceSourceListResolution

Il **metodo ForceSourceListResolution** dell'oggetto [**Installer**](installer-object.md) forza il programma di installazione a cercare un'origine del prodotto valida nell'elenco di origine alla successiva richiesta di un'origine, ad esempio quando il programma di installazione esegue un'installazione o una reinstallazione o quando è necessario il percorso per un set di componenti da eseguire dall'origine.

## <a name="syntax"></a>Sintassi


```JScript
Installer.ForceSourceListResolution(
  Product,
  User
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Prodotto* 
</dt> <dd>

Specifica il codice prodotto.

</dd> <dt>

*Utente* 
</dt> <dd>

Nome utente per l'installazione per utente. Stringa null o vuota per l'installazione per computer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller è definito come \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[Resilienza dell'origine](source-resiliency.md)
</dt> </dl>

 

 




