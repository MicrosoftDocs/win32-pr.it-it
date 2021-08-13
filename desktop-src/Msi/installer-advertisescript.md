---
description: Il metodo AdvertiseScript dell'oggetto Installer annuncia un pacchetto di installazione.
ms.assetid: 45e5268f-7a5f-412f-b9f6-0abb75b79361
title: Metodo Installer::AdvertiseScript
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
ms.openlocfilehash: f6a3ca8b4c07b4bd19b9f5d5066ed17dcc5aa7edb5828741e32ee05197a83777
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633218"
---
# <a name="installeradvertisescript-method"></a>Metodo Installer::AdvertiseScript

Il **metodo AdvertiseScript** dell'oggetto [**Installer**](installer-object.md) annuncia un pacchetto di installazione.

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

Percorso completo del file di script generato dal [**metodo CreateAdvertiseScript.**](installer-createadvertisescript.md)

</dd> <dt>

*scriptFlags* 
</dt> <dd>

Flag che controllano l'annuncio. Questo parametro può essere una combinazione dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                                                                                                           | Significato                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseScriptCacheInfo"></span><span id="msiadvertisescriptcacheinfo"></span><span id="MSIADVERTISESCRIPTCACHEINFO"></span><dl> <dt>**MsiAdvertiseScriptCacheInfo**</dt> <dt>0x001</dt> </dl>                                                                 | Includere questo flag se le icone devono essere create o rimosse.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="msiAdvertiseScriptShortcuts"></span><span id="msiadvertisescriptshortcuts"></span><span id="MSIADVERTISESCRIPTSHORTCUTS"></span><dl> <dt>**msiAdvertiseScriptShortcuts**</dt> <dt>0x004</dt> </dl>                                                                 | Includere questo flag se è necessario creare o rimuovere i collegamenti.<br/>                                                                                                                                                                                                                                                                                                        |
| <span id="msiAdvertiseScriptMachineAssign"></span><span id="msiadvertisescriptmachineassign"></span><span id="MSIADVERTISESCRIPTMACHINEASSIGN"></span><dl> <dt>**msiAdvertiseScriptMachineAssign**</dt> <dt>0x008</dt> </dl>                                                 | Includere questo flag se il prodotto deve essere assegnato a un computer.<br/>                                                                                                                                                                                                                                                                                                        |
| <span id="msiAdvertiseScriptConfigurationRegistration"></span><span id="msiadvertisescriptconfigurationregistration"></span><span id="MSIADVERTISESCRIPTCONFIGURATIONREGISTRATION"></span><dl> <dt>**MsiAdvertiseScriptConfigurationRegistration**</dt> <dt>0x020</dt> </dl> | Includere questo flag se le informazioni di configurazione e gestione nei dati del Registro di sistema devono essere scritte o rimosse.<br/>                                                                                                                                                                                                                                                   |
| <span id="msiAdvertiseScriptValidateTransformList"></span><span id="msiadvertisescriptvalidatetransformlist"></span><span id="MSIADVERTISESCRIPTVALIDATETRANSFORMLIST"></span><dl> <dt>**MsiAdvertiseScriptValidateTransformList**</dt> <dt>0x040</dt> </dl>                 | Includere questo flag per forzare la convalida delle trasformazioni elencate nello script rispetto alle trasformazioni registrate in precedenza per questo prodotto. Si noti che i conflitti di trasformazione vengono rilevati usando un confronto tra stringhe che non fa distinzione tra maiuscole e minuscole e viene valutato tra le installazioni per utente e per computer in tutti i [contesti di installazione.](installation-context.md)<br/> |
| <span id="msiAdvertiseScriptClassInfoRegistration"></span><span id="msiadvertisescriptclassinforegistration"></span><span id="MSIADVERTISESCRIPTCLASSINFOREGISTRATION"></span><dl> <dt>**MsiAdvertiseScriptClassInfoRegistration**</dt> <dt>0x080</dt> </dl>                 | Includere questo flag se le informazioni sugli annunci nel Registro di sistema relative alle classi COM devono essere scritte o rimosse.<br/>                                                                                                                                                                                                                                                    |
| <span id="msiAdvertiseScriptExtensionInfoRegistration"></span><span id="msiadvertisescriptextensioninforegistration"></span><span id="MSIADVERTISESCRIPTEXTENSIONINFOREGISTRATION"></span><dl> <dt>**MsiAdvertiseScriptExtensionInfoRegistration**</dt> <dt>0x100</dt> </dl> | Includere questo flag se le informazioni sugli annunci pubblicitari nel Registro di sistema relative a un'estensione devono essere scritte o rimosse.<br/>                                                                                                                                                                                                                                                   |
| <span id="msiAdvertiseScriptAppInfo"></span><span id="msiadvertisescriptappinfo"></span><span id="MSIADVERTISESCRIPTAPPINFO"></span><dl> <dt>**MsiAdvertiseScriptAppInfo**</dt> <dt>0x180</dt> </dl>                                                                         | Includere questo flag se le informazioni sugli annunci nel Registro di sistema devono essere scritte o rimosse.<br/>                                                                                                                                                                                                                                                                       |
| <span id="msiAdvertiseScriptRegData"></span><span id="msiadvertisescriptregdata"></span><span id="MSIADVERTISESCRIPTREGDATA"></span><dl> <dt>**MsiAdvertiseScriptRegData**</dt> <dt>0x1A0</dt> </dl>                                                                         | Includere questo flag se le informazioni sugli annunci nel Registro di sistema devono essere scritte o rimosse.<br/>                                                                                                                                                                                                                                                                       |



 

</dd> <dt>

*removeItems* 
</dt> <dd>

TRUE se gli elementi specificati devono essere rimossi anziché essere creati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il **metodo AdvertiseScript** usa la [**funzione MsiAdvertiseScript.**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta) L'uso del **metodo AdvertiseScript** richiede che lo script sia in esecuzione all'interno di un processo di sistema locale.

## <a name="examples"></a>Esempio

L'esempio seguente illustra l'uso **del metodo AdvertiseScript.**


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
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione 4.5 in Windows Server 2003 e Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Programma di installazione**](installer-object.md)
</dt> <dt>

[Non supportato in Windows Installer 3.1 e versioni precedenti](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




