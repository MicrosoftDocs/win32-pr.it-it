---
title: Configurazione di estensioni delle unità dati
description: Configurazione di estensioni delle unità dati
ms.assetid: 5dc0a596-68ae-409a-9abc-15ca507d6ec7
keywords:
- flussi, configurazione di estensioni di unità dati
- flussi, estensioni di unità dati
- estensioni unità dati, configurazione
- profili, estensioni di unità dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc7e6794b95128d180bc3922f9bf03a15a2749df
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "103724045"
---
# <a name="configuring-data-unit-extensions"></a>Configurazione di estensioni delle unità dati

Gli esempi scritti nei file ASF possono contenere informazioni aggiuntive oltre agli esempi di supporti. Queste informazioni vengono incluse utilizzando le estensioni di unità dati. Per ulteriori informazioni sulle estensioni dell'unità dati, vedere [estensioni di unità dati](data-unit-extensions.md).

Per usare le estensioni dell'unità dati, è necessario configurare il flusso nel profilo per accettarle. Per configurare un'estensione di unità dati per un flusso, seguire questa procedura.

1.  Ottenere un puntatore all'interfaccia [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) chiamando il metodo **QueryInterface** di [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig).
2.  Chiamare [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) per registrare un tipo di estensione di unità dati per il flusso.

È possibile esaminare tutti i tipi di estensione dell'unità dati attualmente registrati per un flusso chiamando [**IWMStreamConfig2:: GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) per recuperare il numero di tipi di estensione di unità dati registrate. È quindi possibile scorrere in ciclo tutti i tipi usando le chiamate a [**IWMStreamConfig2:: GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) per ognuno di essi.

Alle estensioni delle unità dati viene assegnata una dimensione se configurata per un flusso. Molti sistemi di estensione di unità dati utilizzano dati di dimensioni costanti (in genere una struttura). Tuttavia, è anche possibile configurare le estensioni dell'unità dati in modo che siano di dimensioni variabili impostando la dimensione su 0xFFFF. Ogni estensione dell'unità dati assegnata in fase di codifica può quindi avere dimensioni comprese tra 1 byte e 65534 byte. Le estensioni di unità dati di dimensioni variabili sono denominate anche estensioni di unità dati dinamiche.

Il vantaggio dell'utilizzo delle estensioni di unità dati dinamiche è che è possibile alleghi i dati di estensione in base alle esigenze. Se si definisce un'estensione di unità dati con una dimensione impostata, ogni esempio per il flusso deve contenere dati di estensione di tale dimensione, anche se non sono presenti dati per alcuni esempi. Con le estensioni dell'unità dati dinamica è possibile omettere le estensioni dell'unità dati da alcuni esempi, per risparmiare spazio e ridurre i requisiti di larghezza di banda. Tuttavia, se le estensioni dell'unità dati sono di dimensioni variabili, l'oggetto di lettura non è in grado di verificare i dati di estensione ricevuti in base a una dimensione statica. È necessario verificare che i dati dell'estensione ricevuti siano validi e non la distorsione dannosa del flusso di bit.

Le singole estensioni di unità dati devono essere impostate per gli esempi tramite il metodo [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) . Per altre informazioni, vedere [Setting Data Unit Extensions](setting-data-unit-extensions.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione di flussi**](configuring-streams.md)
</dt> </dl>

 

 




