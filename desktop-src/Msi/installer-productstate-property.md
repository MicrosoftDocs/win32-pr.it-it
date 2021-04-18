---
description: La proprietà ProductState è una proprietà di sola lettura che restituisce le informazioni sullo stato di installazione di un prodotto.
ms.assetid: 9ae3bc86-aa13-41b3-b058-4037607f7dd5
title: Metodo della proprietà Installer. ProductState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cdd1397def1cd25405d0a80a6d5cfde2ee6ef77e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329130"
---
# <a name="installerproductstate-property-method"></a>Metodo della proprietà Installer. ProductState

La **Proprietà ProductState** è una proprietà di sola lettura che restituisce le informazioni sullo stato di installazione di un prodotto.

## <a name="syntax"></a>Sintassi


```JScript
Installer.ProductState Property(
  Product
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Prodotto* 
</dt> <dd>

Specifica il codice del prodotto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Restituisce uno dei valori mostrati nella tabella seguente.



| Stato dell'installazione        | Descrizione                                      |
|---------------------------|--------------------------------------------------|
| msiInstallStateAbsent     | Il prodotto viene installato per un utente diverso.   |
| msiInstallStateDefault    | Il prodotto è installato per l'utente corrente.   |
| msiInstallStateAdvertised | Il prodotto è annunciato ma non è installato.     |
| msiInstallStateInvalidArg | Un parametro non valido è stato passato alla funzione. |
| msiInstallStateUnknown    | Il prodotto non è né annunciato né installato. |
| msiInstallStateBadConfig  | I dati di configurazione sono danneggiati.               |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)
</dt> </dl>

 

 




