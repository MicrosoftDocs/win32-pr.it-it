---
description: La proprietà FeatureState di sola lettura restituisce lo stato di installazione di una funzionalità.
ms.assetid: a3d30296-191e-4446-b5b1-a92f8991926a
title: Proprietà Installer. FeatureState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cf6fe61899ea1daac37fd678e9f0e70dfcc3af69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324635"
---
# <a name="installerfeaturestate-property"></a>Proprietà Installer. FeatureState

La proprietà **FeatureState** di sola lettura restituisce lo stato di installazione di una funzionalità.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.FeatureState
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Questa proprietà restituisce uno dei valori seguenti.



| Valore                     | Descrizione                                      |
|---------------------------|--------------------------------------------------|
| msiInstallStateAbsent     | La funzionalità non è installata.                    |
| msiInstallStateAdvertised | La funzionalità è annunciata.                       |
| msiInstallStateLocal      | La funzionalità è installata per l'esecuzione in locale.         |
| msiInstallStateSource     | La funzionalità è installata per l'esecuzione dall'origine.     |
| msiInstallStateInvalidArg | Un parametro non valido è stato passato alla funzione. |
| msiInstallStateUnknown    | Il codice prodotto o l'ID funzionalità è sconosciuto.       |
| msiInstallStateBadConfig  | I dati di configurazione sono danneggiati.               |



 

 

La proprietà **FeatureState** non verifica che la funzionalità sia accessibile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea)
</dt> </dl>

 

 




