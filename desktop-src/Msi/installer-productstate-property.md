---
description: La proprietà ProductState è una proprietà di sola lettura che restituisce le informazioni sullo stato di installazione per un prodotto.
ms.assetid: 9ae3bc86-aa13-41b3-b058-4037607f7dd5
title: Metodo della proprietà Installer.ProductState
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
ms.openlocfilehash: c19a712c4838905296026a2a0bea4c9e1abc1c49465a854692dd603734e0bd89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763621"
---
# <a name="installerproductstate-property-method"></a>Metodo della proprietà Installer.ProductState

La **proprietà ProductState è** una proprietà di sola lettura che restituisce le informazioni sullo stato di installazione per un prodotto.

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

Specifica il codice prodotto del prodotto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Restituisce uno dei valori illustrati nella tabella seguente.



| Stato dell'installazione        | Descrizione                                      |
|---------------------------|--------------------------------------------------|
| msiInstallStateAbsent     | Il prodotto viene installato per un utente diverso.   |
| msiInstallStateDefault    | Il prodotto viene installato per l'utente corrente.   |
| msiInstallStateAdvertised | Il prodotto viene annunciato ma non installato.     |
| msiInstallStateInvalidArg | Alla funzione è stato passato un parametro non valido. |
| msiInstallStateUnknown    | Il prodotto non viene annunciato né installato. |
| msiInstallStateBadConfig  | I dati di configurazione sono danneggiati.               |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)
</dt> </dl>

 

 




