---
description: Inizializzazione dell'oggetto ContentInfo di un nuovo file ASF
ms.assetid: a4f6c90e-1b38-4c70-8bc5-e2e16af3d87a
title: Inizializzazione dell'oggetto ContentInfo di un nuovo file ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74826942700f4be8028075fcd9466414834eb8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343331"
---
# <a name="initializing-the-contentinfo-object-of-a-new-asf-file"></a>Inizializzazione dell'oggetto ContentInfo di un nuovo file ASF

Dopo aver creato un oggetto ContentInfo vuoto chiamando la funzione [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) , l'applicazione deve chiamare [**IMFASFContentInfo:: seprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) per fornire il profilo di codifica. Per informazioni sulla creazione di un profilo, vedere Creazione di un [profilo ASF](creating-an-asf-profile.md).

Prima di poter leggere le informazioni dal profilo, il metodo **seprofile** deve convalidare l'oggetto profilo specificato controllando gli identificatori di flusso o i tipi di supporto. Se il profilo supera la convalida, vengono generati vari oggetti intestazione, ad esempio l'oggetto proprietà del file, l'oggetto proprietà del flusso di velocità in bit, l'oggetto proprietà del flusso e l'oggetto di esclusione reciproca.

**Seprofile** calcola e imposta i valori consigliati per determinate proprietà, ad esempio il valore di preroll. Se non è già stato impostato, il valore di preroll consigliato in millisecondi dipende dalla finestra massima del buffer del bucket di perdita specificata per i flussi nel profilo. Analogamente, vengono impostate anche le dimensioni dei pacchetti di dati Minimum e Maximum. I valori consigliati potrebbero eseguire l'override delle dimensioni dei pacchetti impostate nel profilo tramite gli attributi.

Poiché è in corso la creazione del file, il file viene categorizzato come tipo di trasmissione, che è indicato dal campo Flags dell'oggetto proprietà file. Alcuni valori sconosciuti, ad esempio il numero di pacchetti di dati, la durata della riproduzione e la durata della trasmissione, sono impostati su zero. Questi valori sono rappresentati dagli attributi **MF \_ PD \_ ASF \_ xxx** e devono essere aggiornati dall'applicazione al termine della creazione del file.

L'oggetto profilo specificato sostituisce qualsiasi profilo esistente associato all'oggetto ContentInfo, rimuove gli oggetti intestazione a cui viene fatto riferimento e reimposta le proprietà globali del file, ad esempio la preroll e la dimensione del pacchetto di dati.

Il metodo **seprofile** crea anche l'oggetto dati che rappresenta l'oggetto dati ASF. Se si riutilizza un oggetto ContentInfo che include informazioni su tutti i pacchetti di dati, il **profilo** non riesce e restituisce l'errore di MF \_ e \_ già \_ inizializzato che indica che è già associato a un oggetto dati ASF esistente. Per impostazione predefinita, per un nuovo oggetto ContentInfo, il numero di pacchetti di dati è impostato su zero e le dimensioni dell'oggetto dati sono impostate su 50 byte. Se si usa il multiplexer per generare pacchetti di dati, il multiplexer aggiorna l'oggetto ContentInfo in modo da riflettere i nuovi valori, ad esempio il numero di pacchetti di dati. Per ulteriori informazioni sulla generazione di pacchetti di dati, vedere [generazione di nuovi pacchetti di dati ASF](generating-new-asf-data-packets.md).

Dopo che tutti gli oggetti Header sono stati aggiunti all'oggetto intestazione ASF finale, è possibile recuperare la dimensione totale dell'intestazione chiamando [**IMFASFContentInfo:: GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize). Questa dimensione include le dimensioni iniziali dell'oggetto dati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione delle proprietà nell'oggetto ContentInfo](setting-properties-in-the-contentinfo-object.md)
</dt> <dt>

[Scrittura di un oggetto intestazione ASF per un nuovo file](writing-an-asf-header-object-for-a-new-file.md)
</dt> </dl>

 

 



