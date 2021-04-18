---
description: Per ogni prodotto elencato dal pacchetto di patch come idoneo per la ricezione della patch, il Metodo ApplyPatch dell'oggetto del programma di installazione richiama un'installazione e imposta la proprietà PATCH sul percorso del pacchetto di patch.
ms.assetid: eee93b6d-f45b-40ae-8e17-cfe6f46b66f4
title: Installer. ApplyPatch, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ApplyPatch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cc1b7509ddb4c61fa84a4547dcd47f2c7637b913
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328317"
---
# <a name="installerapplypatch-method"></a>Installer. ApplyPatch, metodo

Per ogni prodotto elencato dal pacchetto di patch come idoneo per la ricezione della patch, il metodo **applypatch** dell'oggetto del [**programma**](installer-object.md) di installazione richiama un'installazione e imposta la proprietà [**patch**](patch.md) sul percorso del pacchetto di patch.

## <a name="syntax"></a>Sintassi


```JScript
Installer.ApplyPatch(
  PatchPackage,
  InstallPackage,
  InstallType,
  CommandLine
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PacchettoPatch* 
</dt> <dd>

Specifica il percorso del pacchetto di patch.

</dd> <dt>

*InstallPackage* 
</dt> <dd>

Se *InstallType* è impostato su MsiInstallTypeNetworkImage, *InstallPackage* specifica il percorso del prodotto a cui applicare la patch. Se *InstallType* è impostato su MsiInstallTypeDefault e *InstallPackage* è impostato su 0, il programma di installazione applica la patch a tutti i prodotti idonei elencati nel pacchetto di patch.

Se *InstallType* è msiInstallTypeSingleInstance, il programma di installazione applica la patch al prodotto specificato da *InstallPackage*. In questo caso, altri prodotti idonei elencati nel pacchetto di patch vengono ignorati e il parametro *InstallPackage* contiene la stringa con terminazione null che rappresenta il codice prodotto dell'istanza da applicare alla patch. Per questo tipo di installazione è necessario che la versione del Windows Installer fornita con Windows Server 2003 o versione successiva o Windows Installer XP SP1 o versione successiva.

</dd> <dt>

*InstallType* 
</dt> <dd>

Questo parametro specifica il tipo di installazione di cui applicare la patch. Il parametro *InstallType* viene ignorato se *InstallPackage* viene omesso.



| Valore                                                                                                                                                                                                                                            | Significato                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallTypeNetworkImage"></span><span id="msiinstalltypenetworkimage"></span><span id="MSIINSTALLTYPENETWORKIMAGE"></span><dl> <dt>**msiInstallTypeNetworkImage**</dt> </dl> | Indica un'installazione amministrativa. In questo caso, *InstallPackage* deve essere impostato su un percorso del pacchetto. Il valore 1 per msiInstallTypeNetworkImage specifica un'installazione amministrativa.<br/>                                                                                                                                                                                                                    |
| <span id="msiInstallTypeDefault"></span><span id="msiinstalltypedefault"></span><span id="MSIINSTALLTYPEDEFAULT"></span><dl> <dt>**msiInstallTypeDefault**</dt> </dl>                     | Cerca nel sistema i prodotti da applicare alla patch. In questo caso, *InstallPackage* deve essere una stringa vuota.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiInstallSingleInstance"></span><span id="msiinstallsingleinstance"></span><span id="MSIINSTALLSINGLEINSTANCE"></span><dl> <dt>**msiInstallSingleInstance**</dt> </dl>         | Applicare patch al prodotto specificato da *InstallPackage*. *InstallPackage* è il codice prodotto dell'istanza da applicare alla patch. Questo tipo di installazione richiede la versione Windows Installer fornita con Windows Server 2003 o versioni successive o Windows Installer XP SP1 o versione successiva. Per ulteriori informazioni, vedere [installazione di più istanze di prodotti e patch](installing-multiple-instances-of-products-and-patches.md).<br/> |



 

</dd> <dt>

*CommandLine* 
</dt> <dd>

Specifica le impostazioni delle proprietà impostate nella riga di comando. Vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Poiché il delimitatore di elenco per le trasformazioni, le origini e le patch è un punto e virgola, questo carattere non deve essere usato per i nomi file o i percorsi.

La proprietà [**REINSTALL**](reinstall.md) è obbligatoria quando si applica un [aggiornamento di piccole dimensioni](small-updates.md) o una patch di [aggiornamento secondaria](minor-upgrades.md) . Senza questa proprietà, la patch è registrata nel sistema, ma non può aggiornare i file.

**Windows Installer 2,0:** È necessario impostare la proprietà [**REINSTALL**](reinstall.md) nella riga di comando quando si applica una patch di aggiornamento [piccola](small-updates.md) o [secondaria](minor-upgrades.md) . Per le patch che non utilizzano un [tipo di azione personalizzato 51](custom-action-type-51.md) per impostare automaticamente le proprietà **REINSTALL** e [**REINSTALLMODE**](reinstallmode.md) , è necessario impostare in modo esplicito la proprietà **REINSTALL** con il parametro *CommandLine* . Impostare la proprietà **REINSTALL** per elencare le funzionalità interessate dalla patch oppure utilizzare un'impostazione predefinita pratica "reinstall = all". Il valore predefinito della proprietà **REINSTALLMODE** è "omus".

**Windows Installer 3,0 e versioni successive:** A partire da Windows Installer versione 3,0, la proprietà [**REINSTALL**](reinstall.md) viene configurata dal programma di installazione e non deve essere impostata nella riga di comando.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer 3,0 o versioni successive in Windows Server 2003 o Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
</dt> <dt>

[Informazioni sulle proprietà](about-properties.md)
</dt> <dt>

[Non supportato in Windows Installer 2,0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




