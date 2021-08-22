---
description: La proprietà InstallProperty è il valore della proprietà per l'istanza di questo prodotto. Questa proprietà chiama la funzione MsiGetProductInfoEx, con ProductCode, UserSid e Context dell'oggetto Product e la proprietà richiesta come parametro.
ms.assetid: 945c11fe-39da-43b7-a19f-e6364d5e715c
title: Metodo Product.InstallProperty
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.InstallProperty
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3beb67ccdd4a50cdbb52e41846f46fcb4f2545dd833d30098e29c4d5887f8fae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926071"
---
# <a name="productinstallproperty-method"></a>Metodo Product.InstallProperty

La **proprietà InstallProperty** è il valore della proprietà per l'istanza di questo prodotto.

Questa proprietà chiama la [**funzione MsiGetProductInfoEx,**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) con *ProductCode*, *UserSid* e *Context* dell'oggetto [**Product**](product-object.md) e la proprietà richiesta come parametro.

## <a name="syntax"></a>Sintassi


```JScript
Product.InstallProperty(
  property
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*property* 
</dt> <dd>

Specifica la proprietà da recuperare. Le proprietà nell'elenco seguente possono essere recuperate solo da applicazioni già installate. Si noti [che](required-properties.md) le proprietà obbligatorie sono garantite come disponibili, ma altre proprietà sono disponibili solo se tale proprietà è stata impostata. Per informazioni su come [](properties.md) viene impostata ogni proprietà, vedere i collegamenti indicati alle proprietà del programma di installazione.



| Proprietà installate                                                                                                                                                                                                               | Significato                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INSTALLPROPERTY_PRODUCTSTATE"></span><span id="installproperty_productstate"></span><dl> <dt>**INSTALLPROPERTY \_ PRODUCTSTATE**</dt> </dl>                         | Stato del prodotto restituito in formato stringa come "1" per Advertised e "5" per installato.<br/>                                                                                                                                                                                                                                                                            |
| <span id="INSTALLPROPERTY_HELPLINK"></span><span id="installproperty_helplink"></span><dl> <dt>**INSTALLPROPERTY \_ HELPLINK**</dt> </dl>                                     | Collegamento al supporto tecnico. Per altre informazioni, vedere la [**proprietà ARPHELPLINK.**](arphelplink.md)<br/>                                                                                                                                                                                                                                                                             |
| <span id="INSTALLPROPERTY_HELPTELEPHONE"></span><span id="installproperty_helptelephone"></span><dl> <dt>**INSTALLPROPERTY \_ HELPTELEPHONE**</dt> </dl>                      | Telefono del supporto tecnico. Per altre informazioni, vedere la [**proprietà ARPHELPTELEPHONE.**](arphelptelephone.md)<br/>                                                                                                                                                                                                                                                              |
| <span id="INSTALLPROPERTY_INSTALLDATE"></span><span id="installproperty_installdate"></span><dl> <dt>**INSTALLPROPERTY \_ INSTALLDATE**</dt> </dl>                            | Ultima volta in cui il prodotto ha ricevuto il servizio. Il valore di questa proprietà viene sostituito ogni volta che viene applicata o rimossa una patch dal prodotto o viene usata l'opzione della riga di comando [/v](command-line-options.md) per ripristinare il prodotto. Se il prodotto non ha ricevuto alcuna correzione o patch, questa proprietà contiene l'ora in cui il prodotto è stato installato nel computer.<br/> |
| <span id="INSTALLPROPERTY_INSTALLEDPRODUCTNAME"></span><span id="installproperty_installedproductname"></span><dl> <dt>**INSTALLPROPERTY \_ INSTALLEDPRODUCTNAME**</dt> </dl> | Nome del prodotto installato. Per altre informazioni, vedere la [**proprietà ProductName.**](productname.md)<br/>                                                                                                                                                                                                                                                                   |
| <span id="INSTALLPROPERTY_INSTALLLOCATION"></span><span id="installproperty_installlocation"></span><dl> <dt>**INSTALLPROPERTY \_ INSTALLLOCATION**</dt> </dl>                | Percorso di installazione. Per altre informazioni, vedere la [**proprietà ARPINSTALLLOCATION.**](arpinstalllocation.md)<br/>                                                                                                                                                                                                                                                      |
| <span id="INSTALLPROPERTY_INSTALLSOURCE"></span><span id="installproperty_installsource"></span><dl> <dt>**INSTALLPROPERTY \_ INSTALLSOURCE**</dt> </dl>                      | Origine dell'installazione. Per altre informazioni, vedere la [**proprietà SourceDir.**](sourcedir.md)<br/>                                                                                                                                                                                                                                                                          |
| <span id="INSTALLPROPERTY_LOCALPACKAGE"></span><span id="installproperty_localpackage"></span><dl> <dt>**INSTALLPROPERTY \_ LOCALPACKAGE**</dt> </dl>                         | Pacchetto memorizzato nella cache locale.<br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="INSTALLPROPERTY_PUBLISHER"></span><span id="installproperty_publisher"></span><dl> <dt>**INSTALLPROPERTY \_ PUBLISHER**</dt> </dl>                                  | Server di pubblicazione. Per altre informazioni, vedere la [**proprietà Manufacturer.**](manufacturer.md)<br/>                                                                                                                                                                                                                                                                              |
| <span id="INSTALLPROPERTY_URLINFOABOUT"></span><span id="installproperty_urlinfoabout"></span><dl> <dt>**INSTALLPROPERTY \_ URLINFOABOUT**</dt> </dl>                         | Informazioni sull'URL. Per altre informazioni, vedere la [**proprietà ARPURLINFOABOUT.**](arpurlinfoabout.md)<br/>                                                                                                                                                                                                                                                                  |
| <span id="INSTALLPROPERTY_URLUPDATEINFO"></span><span id="installproperty_urlupdateinfo"></span><dl> <dt>**INSTALLPROPERTY \_ URLUPDATEINFO**</dt> </dl>                      | Informazioni sull'aggiornamento dell'URL. Per altre informazioni, vedere la [**proprietà ARPURLUPDATEINFO.**](arpurlupdateinfo.md)<br/>                                                                                                                                                                                                                                                         |
| <span id="INSTALLPROPERTY_VERSIONMINOR"></span><span id="installproperty_versionminor"></span><dl> <dt>**INSTALLPROPERTY \_ VERSIONMINOR**</dt> </dl>                         | Versione secondaria del prodotto derivata dalla [**proprietà ProductVersion.**](productversion.md)<br/>                                                                                                                                                                                                                                                                            |
| <span id="INSTALLPROPERTY_VERSIONMAJOR"></span><span id="installproperty_versionmajor"></span><dl> <dt>**INSTALLPROPERTY \_ VERSIONMAJOR**</dt> </dl>                         | Versione principale del prodotto derivata dalla [**proprietà ProductVersion.**](productversion.md)<br/>                                                                                                                                                                                                                                                                            |
| <span id="INSTALLPROPERTY_VERSIONSTRING"></span><span id="installproperty_versionstring"></span><dl> <dt>**INSTALLPROPERTY \_ VERSIONSTRING**</dt> </dl>                      | Versione del prodotto. Per altre informazioni, vedere la [**proprietà ProductVersion.**](productversion.md)<br/>                                                                                                                                                                                                                                                                    |



 

Per recuperare l'ID prodotto, il proprietario registrato o la  società registrata dalle applicazioni già installate, impostare la proprietà su uno dei valori di stringa di testo seguenti.



| Valore      | Descrizione                                                                                    |
|------------|------------------------------------------------------------------------------------------------|
| ProductID  | Identificatore del prodotto. Per altre informazioni, vedere la [**proprietà ProductID.**](productid.md) |
| RegCompany | La società registrata per l'uso di questo prodotto.                                                    |
| RegOwner   | Proprietario registrato per l'uso di questo prodotto.                                                      |



 

Per recuperare il tipo di istanza del prodotto, *impostare la proprietà* sul valore seguente. Questa proprietà è disponibile per i prodotti annunciati o installati.



| Valore        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Instancetype | Un valore mancante o 0 indica una normale installazione del prodotto. Il valore 1 indica un prodotto installato usando una trasformazione a istanze multiple e la [**proprietà MSINEWINSTANCE.**](msinewinstance.md) Disponibile con il programma di installazione Windows Server 2003 o Windows XP con SP1. Per altre informazioni, vedere [Installazione di più istanze di prodotti e patch.](installing-multiple-instances-of-products-and-patches.md) |



 

Le proprietà nell'elenco seguente possono essere recuperate anche dalle applicazioni annunciate. Queste proprietà non possono essere recuperate per le istanze del prodotto installate in un contesto non gestito per utente per account utente diversi dall'account utente corrente.



| Proprietà annunciate                 | Descrizione                                                                                                                                                                                                                                                                                          |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TRASFORMAZIONI \_ INSTALLPROPERTY           | Trasformazioni.                                                                                                                                                                                                                                                                                          |
| LINGUAGGIO INSTALLPROPERTY \_             | Lingua del prodotto.                                                                                                                                                                                                                                                                                    |
| INSTALLPROPERTY \_ PRODUCTNAME          | Nome del prodotto leggibile. Per altre informazioni, vedere la [**proprietà ProductName.**](productname.md)                                                                                                                                                                                              |
| INSTALLPROPERTY \_ ASSIGNMENTTYPE       | È uguale a zero (0) se il prodotto viene annunciato o installato per utente. È uguale a uno (1) se il prodotto viene annunciato o installato per computer per tutti gli utenti.<br/>                                                                                                                                  |
| INSTALLPROPERTY \_ PACKAGECODE          | Identificatore del pacchetto da cui è stato installato il prodotto. Per informazioni dettagliate, vedere [Codici dei pacchetti.](package-codes.md)                                                                                                                                                                                      |
| VERSIONE \_ INSTALLPROPERTY              | Versione del prodotto derivata dalla [**proprietà ProductVersion.**](productversion.md)                                                                                                                                                                                                                  |
| INSTALLPROPERTY \_ PRODUCTICON          | Icona primaria per il pacchetto. Per altre informazioni, vedere la [**proprietà ARPPRODUCTICON.**](arpproducticon.md)                                                                                                                                                                                       |
| INSTALLPROPERTY \_ PACKAGENAME          | Nome del pacchetto di installazione originale.                                                                                                                                                                                                                                                           |
| INSTALLPROPERTY \_ AUTHORIZED \_ LUA \_ APP | Il valore 1 indica un prodotto che può essere utilizzato da utenti non amministratori tramite l'applicazione di patch a Controllo [dell'account utente.](user-account-control--uac--patching.md) Un valore mancante o 0 indica che l'applicazione di patch con privilegi minimi non è abilitata. Disponibile con Windows Installer 3.0 e versioni successive. |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se la chiamata ha esito positivo, la proprietà contiene il valore come stringa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione 3.0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct è definito come 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Prodotto**](product-object.md)
</dt> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




