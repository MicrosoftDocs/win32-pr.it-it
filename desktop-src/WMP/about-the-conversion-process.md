---
title: Informazioni sul processo di conversione
description: Informazioni sul processo di conversione
ms.assetid: 147b82fd-9e82-4acf-8f8a-43eb02e99024
keywords:
- Media Player Windows, processo di conversione
- Plug-in di Windows Media Player, conversione
- plug-in, conversione
- plug-in di conversione, processo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6fe2f2bbedf03b78c0d19abaf3793e8e92c788
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046325"
---
# <a name="about-the-conversion-process"></a>Informazioni sul processo di conversione

Quando Windows Media Player crea un'istanza del plug-in di conversione, il processo procede come segue:

1.  Il lettore chiama [IWMPConvert:: convertfile](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpconvert-convertfile).
2.  Il plug-in converte il file specificato nel parametro *bstrInputFile* in un formato ASF.
3.  Se per qualche motivo la conversione non riesce, il plug-in restituisce un codice di errore appropriato e il processo viene interrotto.
4.  Se la conversione ha esito positivo, il plug-in inserisce il file convertito nella cartella specificata nel parametro *bstrDestinationFolder* e restituisce il percorso completo del file convertito tramite il parametro *pbstrOutputFile* .
5.  Il plug-in restituisce un codice di esito positivo da **convertfile**.
6.  Il lettore copia il file convertito in una cartella nella gerarchia di cartelle musica dell'utente. Esattamente dove il lettore copia il file in dipende dal contenuto. Come parte di questo processo, il lettore potrebbe rinominare il file.
7.  Il lettore copia il file originale (non convertito) in una cartella nella gerarchia di cartelle musica dell'utente. Come parte di questo processo, il lettore potrebbe rinominare il file. Si tratta della copia del file usato dal giocatore quando l'utente Sincronizza il contenuto dal computer a un dispositivo che richiede il formato di file originale. Questo file è denominato *file shadow*.
8.  Il lettore aggiunge alla libreria informazioni sul file convertito. Ciò include l'impostazione del valore per l'attributo **ShadowFilePath** sul nuovo percorso in cui viene salvato il file shadow.

Se è necessario utilizzare il file convertito, è possibile eseguire una query sulla libreria per recuperare il contenuto utilizzando gli attributi **contentdistributor** e **WM/UniqueFileIdentifier** . Se è necessario utilizzare il file shadow, è comunque necessario recuperare l'oggetto **multimediale** per il file convertito, quindi eseguire una query per l'attributo **ShadowFilePath** . Vedere [aggiunta di metadati ai file convertiti](adding-metadata-to-converted-files.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sui plug-in di conversione**](about-conversion-plug-ins.md)
</dt> <dt>

[**Aggiunta di metadati ai file convertiti**](adding-metadata-to-converted-files.md)
</dt> <dt>

[**Lettura di valori di attributo**](reading-attribute-values.md)
</dt> <dt>

[**Attributo ShadowFilePath**](shadowfilepath-attribute.md)
</dt> <dt>

[**Attributo WM/ContentDistributor**](wm-contentdistributor-attribute.md)
</dt> <dt>

[**Attributo WM/UniqueFileIdentifier**](wm-uniquefileidentifier-attribute.md)
</dt> </dl>

 

 




