---
description: Il metodo AdvertiseScript dell'oggetto Installer annuncia un pacchetto di installazione.
ms.assetid: 45e5268f-7a5f-412f-b9f6-0abb75b79361
title: 'Metodo Installer:: AdvertiseScript'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AdvertiseScript
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7e4ec5afae8d870511c6f91502f8b5844ce135bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328065"
---
# <a name="installeradvertisescript-method"></a>Metodo Installer:: AdvertiseScript

Il metodo **AdvertiseScript** dell'oggetto [**Installer**](installer-object.md) annuncia un pacchetto di installazione.

## <a name="syntax"></a>Sintassi


```JScript
.AdvertiseScript(
  scriptPath,
  scriptFlags,
  removeItems
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*scriptPath* 
</dt> <dd>

Percorso completo del file di script generato dal metodo [**CreateAdvertiseScript**](installer-createadvertisescript.md) .

</dd> <dt>

*scriptFlags* 
</dt> <dd>

Flag che controllano l'annuncio. Questo parametro può essere una combinazione dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                                                                                                           | Significato                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseScriptCacheInfo"></span><span id="msiadvertisescriptcacheinfo"></span><span id="MSIADVERTISESCRIPTCACHEINFO"></span><dl> <dt></dt> <dt>0x001</dt> msiAdvertiseScriptCacheInfo </dl>                                                                 | Includere questo flag se è necessario creare o rimuovere le icone.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="msiAdvertiseScriptShortcuts"></span><span id="msiadvertisescriptshortcuts"></span><span id="MSIADVERTISESCRIPTSHORTCUTS"></span><dl> <dt></dt> <dt>0x004</dt> msiAdvertiseScriptShortcuts </dl>                                                                 | Includere questo flag se i tasti di scelta rapida devono essere creati o rimossi.<br/>                                                                                                                                                                                                                                                                                                        |
| <span id="msiAdvertiseScriptMachineAssign"></span><span id="msiadvertisescriptmachineassign"></span><span id="MSIADVERTISESCRIPTMACHINEASSIGN"></span><dl> <dt></dt> <dt>0x008</dt> msiAdvertiseScriptMachineAssign </dl>                                                 | Includere questo flag se il prodotto deve essere assegnato a un computer.<br/>                                                                                                                                                                                                                                                                                                        |
| <span id="msiAdvertiseScriptConfigurationRegistration"></span><span id="msiadvertisescriptconfigurationregistration"></span><span id="MSIADVERTISESCRIPTCONFIGURATIONREGISTRATION"></span><dl> <dt></dt> <dt>0x020</dt> msiAdvertiseScriptConfigurationRegistration </dl> | Includere questo flag se le informazioni di configurazione e gestione nei dati del registro di sistema devono essere scritte o rimosse.<br/>                                                                                                                                                                                                                                                   |
| <span id="msiAdvertiseScriptValidateTransformList"></span><span id="msiadvertisescriptvalidatetransformlist"></span><span id="MSIADVERTISESCRIPTVALIDATETRANSFORMLIST"></span><dl> <dt></dt> <dt>0x040</dt> msiAdvertiseScriptValidateTransformList </dl>                 | Includere questo flag per forzare la convalida delle trasformazioni elencate nello script in base alle trasformazioni registrate in precedenza per questo prodotto. Si noti che i conflitti di trasformazione vengono rilevati usando un confronto tra stringhe senza distinzione tra maiuscole e minuscole e vengono valutati tra le installazioni per utente e per computer in tutti i [contesti di installazione](installation-context.md).<br/> |
| <span id="msiAdvertiseScriptClassInfoRegistration"></span><span id="msiadvertisescriptclassinforegistration"></span><span id="MSIADVERTISESCRIPTCLASSINFOREGISTRATION"></span><dl> <dt></dt> <dt>0x080</dt> msiAdvertiseScriptClassInfoRegistration </dl>                 | Includere questo flag se le informazioni sull'annuncio nel registro di sistema relative alle classi COM devono essere scritte o rimosse.<br/>                                                                                                                                                                                                                                                    |
| <span id="msiAdvertiseScriptExtensionInfoRegistration"></span><span id="msiadvertisescriptextensioninforegistration"></span><span id="MSIADVERTISESCRIPTEXTENSIONINFOREGISTRATION"></span><dl> <dt></dt> <dt>0x100</dt> msiAdvertiseScriptExtensionInfoRegistration </dl> | Includere questo flag se le informazioni sull'annuncio nel registro di sistema relative a un'estensione devono essere scritte o rimosse.<br/>                                                                                                                                                                                                                                                   |
| <span id="msiAdvertiseScriptAppInfo"></span><span id="msiadvertisescriptappinfo"></span><span id="MSIADVERTISESCRIPTAPPINFO"></span><dl> <dt></dt> <dt>0x180</dt> msiAdvertiseScriptAppInfo </dl>                                                                         | Includere questo flag se le informazioni sull'annuncio nel registro di sistema devono essere scritte o rimosse.<br/>                                                                                                                                                                                                                                                                       |
| <span id="msiAdvertiseScriptRegData"></span><span id="msiadvertisescriptregdata"></span><span id="MSIADVERTISESCRIPTREGDATA"></span><dl> <dt></dt> <dt>0x1A0</dt> msiAdvertiseScriptRegData </dl>                                                                         | Includere questo flag se le informazioni sull'annuncio nel registro di sistema devono essere scritte o rimosse.<br/>                                                                                                                                                                                                                                                                       |



 

</dd> <dt>

*removeItems* 
</dt> <dd>

TRUE se gli elementi specificati devono essere rimossi anziché essere creati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il metodo **AdvertiseScript** usa la funzione [**MsiAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta) . Per usare il metodo **AdvertiseScript** è necessario che lo script sia in esecuzione in un processo di sistema locale.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo del metodo **AdvertiseScript** .


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' Advertise Simple package using an advertise script
'   created by CreateAdvertiseScript Method
'
'  Flags 424 indicate msiAdvertiseScriptMachineAssign, msiAdvertiseScriptRegData

Installer.AdvertiseScript "c:\scratch\simpletst\rtm\simple.aas", 424, false

' Verify Simple is installed
MsgBox Installer.ProductState("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}")

'
' Remove Simple using advertise script
'
Installer.AdvertiseScript "c:\scratch\simpletst\rtm\simple.aas", 424, true

' Verify simple is removed
MsgBox Installer.ProductState("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}")
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer 4,5 in Windows Server 2003 e Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Programma di installazione**](installer-object.md)
</dt> <dt>

[Non supportato in Windows Installer 3,1 e versioni precedenti](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




