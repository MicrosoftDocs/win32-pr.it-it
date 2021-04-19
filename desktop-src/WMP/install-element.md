---
title: Elemento install
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. L'elemento install specifica i valori usati da Windows Media Player per installare un archivio online.
ms.assetid: 9a5e15ee-ec36-48d3-a1c2-bf20b6d2da48
keywords:
- Installare gli elementi di Windows Media Player
topic_type:
- apiref
api_name:
- Install Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bba56240651f789b45c18b006b16e5e07b10676e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325444"
---
# <a name="install-element"></a>Elemento install

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

L'elemento **Install** specifica i valori usati da Windows Media Player per installare un archivio online.

``` syntax
<Install
    EULAURL = "URL"
    CodeURL = "URL"
    PrivacyInfoURL = "URL"
    InstallApp = "filename"
    InstallData = "commandline"
    CatalogURL = "URL"
/>
```

## <a name="attributes"></a>Attributi

<dl> <dt>

<span id="EULAURL__required_"></span><span id="eulaurl__required_"></span><span id="EULAURL__REQUIRED_"></span>**EULAURL** (obbligatorio)
</dt> <dd>

URL completo di un file con estensione txt utilizzato da Windows Media Player per visualizzare un contratto di licenza con l'utente finale (EULA). Questo file deve essere codificato in formato ANSI.

</dd> <dt>

<span id="CodeURL__required_"></span><span id="codeurl__required_"></span><span id="CODEURL__REQUIRED_"></span>**CodeURL** (obbligatorio)
</dt> <dd>

URL completo di un pacchetto, con estensione cab, usato per installare l'archivio online. Il pacchetto e tutti i moduli di codice nel pacchetto devono essere firmati. Per informazioni sulla firma del codice, vedere [Introduzione alla firma del codice](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) in MSDN Library.

</dd> <dt>

<span id="PrivacyInfoURL__required_"></span><span id="privacyinfourl__required_"></span><span id="PRIVACYINFOURL__REQUIRED_"></span>**PrivacyInfoURL** (obbligatorio)
</dt> <dd>

URL completo per una pagina Web che contiene informazioni sulla privacy per il negozio online.

</dd> <dt>

<span id="InstallApp__required_"></span><span id="installapp__required_"></span><span id="INSTALLAPP__REQUIRED_"></span>**InstallApp** (obbligatorio)
</dt> <dd>

Nome del file EXE o INF da eseguire. Questo file deve essere contenuto nel file CAB specificato dall'attributo **CodeURL** .

</dd> <dt>

<span id="InstallData__optional_"></span><span id="installdata__optional_"></span><span id="INSTALLDATA__OPTIONAL_"></span>**InstallData** (facoltativo)
</dt> <dd>

Stringa della riga di comando che viene passata all'applicazione specificata dall'attributo **installApp** . Questo attributo è applicabile solo quando il valore di **installApp** specifica un eseguibile.

</dd> <dt>

<span id="CatalogURL__required_for_type_1__ignored_for_type_2_"></span><span id="catalogurl__required_for_type_1__ignored_for_type_2_"></span><span id="CATALOGURL__REQUIRED_FOR_TYPE_1__IGNORED_FOR_TYPE_2_"></span>**CatalogURL** (obbligatorio per il tipo 1, ignorato per il tipo 2)
</dt> <dd>

URL completo per il catalogo compilato del negozio online.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elemento         |
|-----------------|-----------------|
| Elementi padre | **ServiceInfo** |
| Elementi figlio  | nessuno            |



 

## <a name="remarks"></a>Osservazioni

Se uno degli attributi richiesti risulta mancante o non disponibile, il programma di installazione di Windows Media Player non tenterà di scaricare e installare il codice del provider del negozio online. Il programma di installazione configurerà i valori predefiniti offline come specificato nel documento **ServiceInfo** . **ServiceInfo** può essere usata quando non si è connessi a Internet passando il nome del provider predefinito e le informazioni di **ServiceInfo** come parametri della riga di comando. Per informazioni dettagliate sulle opzioni della riga di comando, vedere [ridistribuzione del software Windows Media Player](redistributing-windows-media-player-software.md) .

> [!Note]  
> L'uso di questo elemento richiede la firma di un contratto di ridistribuzione con Microsoft. Per informazioni dettagliate, contattare il rappresentante aziendale.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------|
| Versione<br/> | Windows Media Player 10 o versione successiva.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Documento ServiceInfo di esempio per un negozio online di tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo di esempio per un negozio online di tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

