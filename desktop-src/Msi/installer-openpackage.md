---
description: Il metodo OpenPackage dell'oggetto Installer apre un pacchetto di installazione da usare con funzioni che accedono al database del prodotto e installano il motore, restituendo un oggetto Session.
ms.assetid: 22b03bde-29ae-4dd4-a41c-d55b3a4f424c
title: Installer. OpenPackage, metodo
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
ms.openlocfilehash: 621fac51155b2ac89eba40d39da6d5af6c305e67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324607"
---
# <a name="installeropenpackage-method"></a>Installer. OpenPackage, metodo

Il metodo **OpenPackage** dell'oggetto [**Installer**](installer-object.md) apre un pacchetto di installazione da usare con funzioni che accedono al database del prodotto e installano il motore, restituendo un oggetto [**Session**](session-object.md) .

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

Valore integer facoltativo che specifica se **OpenPackage** deve ignorare lo stato corrente del computer durante la creazione dell'oggetto sessione. Nessun valore o un valore pari a 0 per le opzioni per impostazione predefinita è il comportamento originale. Quando options è 1, il metodo **OpenPackage** ignora lo stato corrente del computer all'apertura del pacchetto. Il valore 1 impedisce le modifiche allo stato corrente del computer. Per ulteriori informazioni, vedere [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il metodo **OpenPackage** può accettare direttamente l'handle di database anziché la stringa per il percorso del pacchetto.

Si noti che solo un oggetto [**sessione**](session-object.md) può essere aperto da un singolo processo. Non è possibile usare **OpenPackage** in un'azione personalizzata perché l'installazione attiva è l'unica sessione consentita.

Un oggetto [**sessione**](session-object.md) sicuro ignora lo stato corrente del computer quando si apre il pacchetto e impedisce le modifiche allo stato corrente del computer. Per ulteriori informazioni, vedere [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




