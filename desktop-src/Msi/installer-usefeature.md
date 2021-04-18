---
description: Il metodo UseFeature dell'oggetto Installer incrementa il conteggio di utilizzo per una particolare funzionalità e restituisce lo stato di installazione per tale funzionalità. Questo metodo deve essere usato per indicare l'intenzione di un'applicazione di usare una funzionalità.
ms.assetid: c9ea812c-2f95-4ba4-ad8e-b96f7fc14bb1
title: Installer. UseFeature, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.UseFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 355e7f4e64a5cb69ffc0371473cb0db1ac6313a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332164"
---
# <a name="installerusefeature-method"></a>Installer. UseFeature, metodo

Il metodo **UseFeature** dell'oggetto [**Installer**](installer-object.md) incrementa il conteggio di utilizzo per una particolare funzionalità e restituisce lo stato di installazione per tale funzionalità. Questo metodo deve essere usato per indicare l'intenzione di un'applicazione di usare una funzionalità.

## <a name="syntax"></a>Sintassi


```JScript
Installer.UseFeature(
  Product,
  Feature,
  InstallMode
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Prodotto* 
</dt> <dd>

Specifica il codice del prodotto.

</dd> <dt>

*Funzionalità* 
</dt> <dd>

Identifica la funzionalità da utilizzare.

</dd> <dt>

*InstallMode* 
</dt> <dd>

Questo parametro deve essere *msiInstallModeNoDetection*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il metodo **UseFeature** deve essere usato solo su funzionalità note per la pubblicazione. L'applicazione deve determinare lo stato della funzionalità chiamando la proprietà [**FeatureState**](installer-featurestate.md) o la proprietà [**features**](installer-features.md) o i rispettivi equivalenti API.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiUseFeatureEx**](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)
</dt> </dl>

 

 




