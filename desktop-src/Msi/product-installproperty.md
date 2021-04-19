---
description: La proprietà InstallProperty è il valore della proprietà per l'istanza di questo prodotto. Questa proprietà chiama la funzione MsiGetProductInfoEx con ProductCode, UserSid e Context dell'oggetto Product e la proprietà richiesta come parametro.
ms.assetid: 945c11fe-39da-43b7-a19f-e6364d5e715c
title: Metodo Product. InstallProperty
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
ms.openlocfilehash: 12949997363fce8073c15f7ca6b7312c211fa0f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325888"
---
# <a name="productinstallproperty-method"></a>Metodo Product. InstallProperty

La proprietà **InstallProperty** è il valore della proprietà per l'istanza di questo prodotto.

Questa proprietà chiama la funzione [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) con *ProductCode*, *UserSID* e *context* dell'oggetto [**Product**](product-object.md) e la proprietà richiesta come parametro.

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

Specifica la proprietà da recuperare. È possibile recuperare le proprietà nell'elenco seguente solo da applicazioni già installate. Si noti che le proprietà [obbligatorie](required-properties.md) sono sicuramente disponibili, ma altre proprietà sono disponibili solo se tale proprietà è stata impostata. Per informazioni sulla modalità di impostazione di ciascuna proprietà, vedere i collegamenti indicati alle [Proprietà](properties.md) del programma di installazione.



| Proprietà installate                                                                                                                                                                                                               | Significato                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INSTALLPROPERTY_PRODUCTSTATE"></span><span id="installproperty_productstate"></span><dl> <dt>**\_PRODUCTSTATE INSTALLPROPERTY**</dt> </dl>                         | Stato del prodotto restituito in formato stringa come "1" per annunciato e "5" per installato.<br/>                                                                                                                                                                                                                                                                            |
| <span id="INSTALLPROPERTY_HELPLINK"></span><span id="installproperty_helplink"></span><dl> <dt>**INSTALLPROPERTY \_ HELPLINK**</dt> </dl>                                     | Collegamento al supporto tecnico. Per ulteriori informazioni, vedere la proprietà [**ARPHELPLINK**](arphelplink.md) .<br/>                                                                                                                                                                                                                                                                             |
| <span id="INSTALLPROPERTY_HELPTELEPHONE"></span><span id="installproperty_helptelephone"></span><dl> <dt>**\_HELPTELEPHONE INSTALLPROPERTY**</dt> </dl>                      | Telefono del supporto tecnico. Per ulteriori informazioni, vedere la proprietà [**ARPHELPTELEPHONE**](arphelptelephone.md) .<br/>                                                                                                                                                                                                                                                              |
| <span id="INSTALLPROPERTY_INSTALLDATE"></span><span id="installproperty_installdate"></span><dl> <dt>**\_INSTALLDATE INSTALLPROPERTY**</dt> </dl>                            | L'ultima volta in cui il prodotto ha ricevuto il servizio. Il valore di questa proprietà viene sostituito ogni volta che una patch viene applicata o rimossa dal prodotto oppure viene utilizzata l' [opzione della riga di comando](command-line-options.md) /v per ripristinare il prodotto. Se il prodotto non ha ricevuto alcuna riparazione o patch, questa proprietà contiene l'ora in cui questo prodotto è stato installato nel computer.<br/> |
| <span id="INSTALLPROPERTY_INSTALLEDPRODUCTNAME"></span><span id="installproperty_installedproductname"></span><dl> <dt>**\_INSTALLEDPRODUCTNAME INSTALLPROPERTY**</dt> </dl> | Nome del prodotto installato. Per ulteriori informazioni, vedere la proprietà [**ProductName**](productname.md) .<br/>                                                                                                                                                                                                                                                                   |
| <span id="INSTALLPROPERTY_INSTALLLOCATION"></span><span id="installproperty_installlocation"></span><dl> <dt>**\_INSTALLLOCATION INSTALLPROPERTY**</dt> </dl>                | Percorso di installazione. Per ulteriori informazioni, vedere la proprietà [**ARPINSTALLLOCATION**](arpinstalllocation.md) .<br/>                                                                                                                                                                                                                                                      |
| <span id="INSTALLPROPERTY_INSTALLSOURCE"></span><span id="installproperty_installsource"></span><dl> <dt>**\_INSTALLSOURCE INSTALLPROPERTY**</dt> </dl>                      | Origine dell'installazione. Per ulteriori informazioni, vedere la proprietà [**SourceDir**](sourcedir.md) .<br/>                                                                                                                                                                                                                                                                          |
| <span id="INSTALLPROPERTY_LOCALPACKAGE"></span><span id="installproperty_localpackage"></span><dl> <dt>**\_LOCALPACKAGE INSTALLPROPERTY**</dt> </dl>                         | Pacchetto locale memorizzato nella cache.<br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="INSTALLPROPERTY_PUBLISHER"></span><span id="installproperty_publisher"></span><dl> <dt>**\_server di pubblicazione INSTALLPROPERTY**</dt> </dl>                                  | Server di pubblicazione. Per ulteriori informazioni, vedere la proprietà del [**produttore**](manufacturer.md) .<br/>                                                                                                                                                                                                                                                                              |
| <span id="INSTALLPROPERTY_URLINFOABOUT"></span><span id="installproperty_urlinfoabout"></span><dl> <dt>**\_URLINFOABOUT INSTALLPROPERTY**</dt> </dl>                         | Informazioni sull'URL. Per ulteriori informazioni, vedere la proprietà [**ARPURLINFOABOUT**](arpurlinfoabout.md) .<br/>                                                                                                                                                                                                                                                                  |
| <span id="INSTALLPROPERTY_URLUPDATEINFO"></span><span id="installproperty_urlupdateinfo"></span><dl> <dt>**\_URLUPDATEINFO INSTALLPROPERTY**</dt> </dl>                      | Informazioni sull'aggiornamento dell'URL. Per ulteriori informazioni, vedere la proprietà [**ARPURLUPDATEINFO**](arpurlupdateinfo.md) .<br/>                                                                                                                                                                                                                                                         |
| <span id="INSTALLPROPERTY_VERSIONMINOR"></span><span id="installproperty_versionminor"></span><dl> <dt>**\_VERSIONMINOR INSTALLPROPERTY**</dt> </dl>                         | Versione secondaria del prodotto derivata dalla proprietà [**ProductVersion**](productversion.md) .<br/>                                                                                                                                                                                                                                                                            |
| <span id="INSTALLPROPERTY_VERSIONMAJOR"></span><span id="installproperty_versionmajor"></span><dl> <dt>**\_Proprietà VERSIONMAJOR INSTALLPROPERTY**</dt> </dl>                         | Versione principale del prodotto derivata dalla proprietà [**ProductVersion**](productversion.md) .<br/>                                                                                                                                                                                                                                                                            |
| <span id="INSTALLPROPERTY_VERSIONSTRING"></span><span id="installproperty_versionstring"></span><dl> <dt>**\_VERSIONSTRING INSTALLPROPERTY**</dt> </dl>                      | Versione del prodotto. Per ulteriori informazioni, vedere la proprietà [**ProductVersion**](productversion.md) .<br/>                                                                                                                                                                                                                                                                    |



 

Per recuperare l'ID prodotto, il proprietario registrato o la società registrata dalle applicazioni già installate, impostare la *Proprietà* su uno dei valori stringa di testo seguenti.



| Valore      | Descrizione                                                                                    |
|------------|------------------------------------------------------------------------------------------------|
| ProductID  | Identificatore del prodotto. Per ulteriori informazioni, vedere la proprietà [**ProductID**](productid.md) . |
| RegCompany | Azienda registrata per l'utilizzo del prodotto.                                                    |
| RegOwner   | Proprietario registrato per utilizzare questo prodotto.                                                      |



 

Per recuperare il tipo di istanza del prodotto, impostare *Property* sul valore seguente. Questa proprietà è disponibile per i prodotti annunciati o installati.



| Valore        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InstanceType | Un valore mancante o un valore pari a 0 indica una normale installazione del prodotto. Il valore 1 indica un prodotto installato utilizzando una trasformazione a più istanze e la proprietà [**MSINEWINSTANCE**](msinewinstance.md) . Disponibile con il programma di installazione che esegue Windows Server 2003 o Windows XP con SP1. Per ulteriori informazioni, vedere [installazione di più istanze di prodotti e patch](installing-multiple-instances-of-products-and-patches.md). |



 

Le proprietà nell'elenco seguente possono anche essere recuperate dalle applicazioni annunciate. Queste proprietà non possono essere recuperate per le istanze di prodotto installate in un contesto non gestito per utente per account utente diversi dall'account utente corrente.



| Proprietà annunciate                 | Descrizione                                                                                                                                                                                                                                                                                          |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_TRASformazioni INSTALLPROPERTY           | Trasformazioni.                                                                                                                                                                                                                                                                                          |
| \_lingua INSTALLPROPERTY             | Lingua del prodotto.                                                                                                                                                                                                                                                                                    |
| INSTALLPROPERTY \_ ProductName          | Leggibile: nome del prodotto. Per ulteriori informazioni, vedere la proprietà [**ProductName**](productname.md) .                                                                                                                                                                                              |
| \_ASSIGNMENTTYPE INSTALLPROPERTY       | È uguale a zero (0) se il prodotto è annunciato o installato per utente. È uguale a uno (1) se il prodotto viene annunciato o installato per computer per tutti gli utenti.<br/>                                                                                                                                  |
| \_PACKAGECODE INSTALLPROPERTY          | Identificatore del pacchetto da cui è stato installato il prodotto. Per informazioni dettagliate, vedere [codici di pacchetto](package-codes.md).                                                                                                                                                                                      |
| versione di INSTALLPROPERTY \_              | Versione del prodotto derivata dalla proprietà [**ProductVersion**](productversion.md) .                                                                                                                                                                                                                  |
| \_PRODUCTICON INSTALLPROPERTY          | Icona primaria per il pacchetto. Per ulteriori informazioni, vedere la proprietà [**arpproducticon**](arpproducticon.md) .                                                                                                                                                                                       |
| INSTALLPROPERTY \_ PackageName          | Nome del pacchetto di installazione originale.                                                                                                                                                                                                                                                           |
| \_app Lua autorizzata INSTALLPROPERTY \_ \_ | Il valore 1 indica un prodotto che può essere gestito da utenti non amministratori mediante l'applicazione di [patch al controllo dell'account utente](user-account-control--uac--patching.md). Un valore mancante o un valore pari a 0 indica che l'applicazione di patch con privilegi minimi non è abilitata. Disponibile con Windows Installer 3,0 e versioni successive. |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se la chiamata ha esito positivo, la proprietà contiene il valore come stringa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct è definito come 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Prodotto**](product-object.md)
</dt> <dt>

[Non supportato in Windows Installer 2,0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




