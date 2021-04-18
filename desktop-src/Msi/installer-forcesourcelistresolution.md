---
description: Il metodo ForceSourceListResolution dell'oggetto Installer impone all'Windows Installer di eseguire la ricerca nell'elenco di origine di una fonte di prodotto valida.
ms.assetid: d5097331-8cf5-494f-9e88-bcffcad3fe5d
title: Installer. ForceSourceListResolution, metodo
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
ms.openlocfilehash: cadc27f3eaa90cd6fb2729f73d07cbcfa1f96b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324619"
---
# <a name="installerforcesourcelistresolution-method"></a>Installer. ForceSourceListResolution, metodo

Il metodo **ForceSourceListResolution** dell'oggetto [**Installer**](installer-object.md) impone al programma di installazione di eseguire la ricerca nell'elenco di origine di una fonte di prodotto valida la volta successiva che è necessaria un'origine, ad esempio quando il programma di installazione esegue un'installazione o una reinstallazione o quando richiede il percorso di un componente impostato per l'esecuzione dall'origine.

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

Specifica il codice del prodotto.

</dd> <dt>

*Utente* 
</dt> <dd>

Nome utente per l'installazione per utente; stringa null o vuota per l'installazione per computer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[Resilienza di origine](source-resiliency.md)
</dt> </dl>

 

 




