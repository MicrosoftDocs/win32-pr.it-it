---
description: Il metodo OpenPackage dell'oggetto Installer apre un pacchetto del programma di installazione da usare con le funzioni che accedono al database del prodotto e al motore di installazione, restituiscono un oggetto Session.
ms.assetid: 22b03bde-29ae-4dd4-a41c-d55b3a4f424c
title: Metodo Installer.OpenPackage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenPackage
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: bc3e96fe55e37a55d5601a0a2d702e6a98582879bf2cff65ee52b5ca6bdc1772
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119388151"
---
# <a name="installeropenpackage-method"></a>Metodo Installer.OpenPackage

Il **metodo OpenPackage** dell'oggetto [**Installer**](installer-object.md) apre un pacchetto del programma di installazione da usare con le funzioni che accedono al database del prodotto e al motore di installazione, restituiscono un [**oggetto Session.**](session-object.md)

## <a name="syntax"></a>Sintassi


```JScript
Installer.OpenPackage(
  packagePath,
  options
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*packagePath* 
</dt> <dd>

Stringa obbligatoria contenente il nome del percorso del pacchetto.

</dd> <dt>

*options* 
</dt> <dd>

Valore intero facoltativo che specifica se **OpenPackage** deve ignorare o meno lo stato corrente del computer durante la creazione dell'oggetto Session. Nessun valore o valore 0 per le opzioni ha come impostazione predefinita il comportamento originale. Quando le opzioni sono 1, il **metodo OpenPackage** ignora lo stato corrente del computer all'apertura del pacchetto. Il valore 1 impedisce modifiche allo stato corrente del computer. Per altre informazioni, vedere [**MsiOpenPackageEx.**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il **metodo OpenPackage** può accettare direttamente l'handle del database anziché la stringa per il percorso del pacchetto.

Si noti che un [**solo oggetto Session**](session-object.md) può essere aperto da un singolo processo. **Non è possibile** usare OpenPackage in un'azione personalizzata perché l'installazione attiva è l'unica sessione consentita.

Un oggetto [**Session**](session-object.md) sicuro ignora lo stato corrente del computer all'apertura del pacchetto e impedisce modifiche allo stato corrente del computer. Per altre informazioni, vedere [**MsiOpenPackageEx.**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller è definito come \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




