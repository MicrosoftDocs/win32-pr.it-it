---
description: Inizializzazione dell'oggetto ContentInfo di un nuovo file ASF
ms.assetid: a4f6c90e-1b38-4c70-8bc5-e2e16af3d87a
title: Inizializzazione dell'oggetto ContentInfo di un nuovo file ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf0180eb4e9369447355a9a4cd607f630bfb3664108ad77d6d008c281f92fdf1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114251"
---
# <a name="initializing-the-contentinfo-object-of-a-new-asf-file"></a>Inizializzazione dell'oggetto ContentInfo di un nuovo file ASF

Dopo aver creato un oggetto ContentInfo vuoto chiamando la funzione [**MFCreateASFContentInfo,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) l'applicazione deve chiamare [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) per fornire il profilo di codifica. Per informazioni sulla creazione di un profilo, vedere [Creazione di un profilo ASF.](creating-an-asf-profile.md)

Prima che le informazioni possano essere lette dal profilo, il **metodo SetProfile** deve convalidare l'oggetto profilo specificato controllando gli identificatori di flusso o i tipi di supporti. Se il profilo supera la convalida, vengono generati vari oggetti intestazione, ad esempio l'oggetto Proprietà file, l'oggetto Proprietà velocità in bit del flusso, l'oggetto proprietà flusso e l'oggetto di esclusione reciproca.

**SetProfile** calcola e imposta i valori consigliati per determinate proprietà, ad esempio il valore di preroll. Se questa opzione non è già impostata, il valore di preroll consigliato in millisecondi dipende dalla finestra massima del buffer del bucket persa specificato per i flussi nel profilo. Analogamente, vengono impostate anche le dimensioni minime e massime dei pacchetti di dati. I valori consigliati potrebbero sostituire le dimensioni dei pacchetti impostate nel profilo tramite attributi.

Poiché il file è in fase di creazione, il file viene categorizzato come tipo di trasmissione, come indica il campo Flag dell'oggetto Proprietà file. Alcuni valori sconosciuti, ad esempio il numero di pacchetti di dati, la durata di riproduzione e la durata dell'invio, sono impostati su zero. Questi valori sono rappresentati dagli attributi xxx di **\_ MF PD \_ ASF \_** e devono essere aggiornati dall'applicazione al termine della creazione del file.

L'oggetto profilo specificato sostituisce qualsiasi profilo esistente associato all'oggetto ContentInfo, rimuove gli oggetti intestazione a cui si fa riferimento e reimposta le proprietà globali del file, ad esempio preroll e dimensioni del pacchetto di dati.

Il **metodo SetProfile** crea anche l'oggetto dati che rappresenta l'oggetto dati ASF. Se si riutilizza un oggetto ContentInfo che include informazioni sui pacchetti di dati, **SetProfile** ha esito negativo e restituisce l'errore MF E ALREADY INITIALIZED che indica che è già associato a un oggetto dati \_ \_ \_ ASF esistente. Per impostazione predefinita, per un nuovo oggetto ContentInfo, il numero di pacchetti di dati è impostato su zero e la dimensione dell'oggetto dati è impostata su 50 byte. Se si usa il multiplexer per generare pacchetti di dati, il multiplexer aggiorna l'oggetto ContentInfo in modo da riflettere i nuovi valori, ad esempio il numero di pacchetti di dati. Per altre informazioni sulla generazione di pacchetti di dati, vedere [Generating New ASF Data Packets](generating-new-asf-data-packets.md).

Dopo aver aggiunto tutti gli oggetti Intestazione all'oggetto intestazione ASF finale, è possibile recuperare le dimensioni totali dell'intestazione chiamando [**IMFASFContentInfo::GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize). Queste dimensioni includono le dimensioni iniziali dell'oggetto dati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione delle proprietà nell'oggetto ContentInfo](setting-properties-in-the-contentinfo-object.md)
</dt> <dt>

[Scrittura di un oggetto intestazione ASF per un nuovo file](writing-an-asf-header-object-for-a-new-file.md)
</dt> </dl>

 

 



