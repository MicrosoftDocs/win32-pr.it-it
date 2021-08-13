---
description: La proprietà FeatureState di sola lettura restituisce lo stato installato di una funzionalità.
ms.assetid: a3d30296-191e-4446-b5b1-a92f8991926a
title: Proprietà Installer.FeatureState
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
ms.openlocfilehash: 989abe860848b943e77b02910e9760f8fcaecc97fd8a2634f8147605577613d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631275"
---
# <a name="installerfeaturestate-property"></a>Proprietà Installer.FeatureState

La proprietà **FeatureState** di sola lettura restituisce lo stato installato di una funzionalità.

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
| msiInstallStateAdvertised | La funzionalità viene annunciata.                       |
| msiInstallStateLocal      | La funzionalità viene installata per l'esecuzione in locale.         |
| msiInstallStateSource     | La funzionalità viene installata per l'esecuzione dall'origine.     |
| msiInstallStateInvalidArg | Alla funzione è stato passato un parametro non valido. |
| msiInstallStateUnknown    | Il codice prodotto o l'ID funzionalità è sconosciuto.       |
| msiInstallStateBadConfig  | I dati di configurazione sono danneggiati.               |



 

 

La **proprietà FeatureState** non convalida che la funzionalità sia accessibile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller è definito come \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea)
</dt> </dl>

 

 




