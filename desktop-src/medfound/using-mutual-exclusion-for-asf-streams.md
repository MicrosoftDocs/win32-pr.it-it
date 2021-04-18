---
description: Uso dell'esclusione reciproca per i flussi ASF
ms.assetid: fdd31eac-1dd6-45f0-90fb-d5a74c85db2e
title: Uso dell'esclusione reciproca per i flussi ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411b5aa0638ab1c56298b93d01e8de99920abc6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310175"
---
# <a name="using-mutual-exclusion-for-asf-streams"></a>Uso dell'esclusione reciproca per i flussi ASF

Il contenuto ASF può contenere più flussi che si escludono a vicenda. Questi flussi non possono essere letti contemporaneamente, ma solo uno di essi viene letto alla volta. Ad esempio, il file può contenere un set di flussi che include lo stesso contenuto codificato a una velocità in bit diversa. Il flusso usato è determinato dalla larghezza di banda disponibile per l'applicazione che trasmette il contenuto. L'oggetto di esclusione reciproca ASF, che fa parte dell'oggetto Header, archivia le informazioni sul gruppo di flussi che si escludono a vicenda.

In Media Foundation, l'oggetto di *esclusione reciproca* che espone l'interfaccia [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion) esiste per ogni oggetto di esclusione reciproca ASF. L'oggetto profilo include riferimenti a tutti gli oggetti di esclusione reciproca.

L'oggetto di esclusione reciproca archivia le informazioni sul gruppo di flussi che si escludono a vicenda come record. Un oggetto di esclusione reciproca può avere più record che possono essere usati per creare scenari complessi. Ogni record contiene uno o più flussi che non possono coesistere con i flussi in un altro record, gestiti dall'oggetto di esclusione reciproca, a seconda del tipo di esclusione reciproca, ad esempio velocità in bit.

Un esempio comune di esclusione reciproca complessa è un file che contiene tre flussi audio dello stesso contenuto a diverse velocità in bit in ognuna delle tre lingue. È necessario riprodurre solo uno dei nove flussi alla volta, ma esistono due tipi per cui si escludono a vicenda: lingua e velocità in bit.

Per questo esempio, ai nove flussi vengono assegnati i numeri di flusso seguenti:

<dl> 1-lingua 1, velocità in bit 1  
2-lingua 1, velocità in bit 2  
3-lingua 1, velocità in bit 3  
4-lingua 2, velocità in bit 1  
5-lingua 2, velocità in bit 2  
6-lingua 2, velocità in bit 3  
7-lingua 3, velocità in bit 1  
8-lingua 3, bit rate 2  
9-lingua 3, bit rate 3  
</dl>

Questo scenario può essere implementato usando i quattro oggetti di esclusione reciproca seguenti:

-   Il primo oggetto di esclusione reciproca include i flussi 1, 2 e 3, che si escludono a vicenda in base alla velocità in bit. Ogni flusso ha un proprio record.
-   Il secondo oggetto di esclusione reciproca include i flussi 4, 5 e 6, che si escludono a vicenda in base alla velocità in bit. Ogni flusso ha un proprio record.
-   Il terzo oggetto di esclusione reciproca include 7, 8 e 9, che si escludono a vicenda in base alla velocità in bit. Ogni flusso ha un proprio record.
-   Il quarto oggetto di esclusione reciproca contiene tre record, il primo include i flussi 1, 2 e 3. il secondo include i flussi 4, 5 e 6; e il terzo, inclusi i flussi 7, 8 e 9. Questi record si escludono a vicenda dal linguaggio.

Quando si riproduce un file creato in questo modo, l'applicazione di streaming seleziona innanzitutto la lingua perché è meno probabile che cambi al centro della presentazione, quindi seleziona una velocità in bit.

## <a name="mutual-exclusion-object-creation-and-configuration"></a>Creazione e configurazione di oggetti di esclusione reciproca

Nell'elenco seguente viene riepilogato il processo di configurazione di un oggetto di esclusione reciproca:

1.  Creare un oggetto di esclusione reciproca.
2.  Impostare il tipo di esclusione reciproca.
3.  Configurare l'oggetto di esclusione reciproca aggiungendo record e i flussi associati.
4.  Aggiungere l'oggetto di esclusione reciproca al profilo.

Per creare e configurare un oggetto di esclusione reciproca

1.  Chiamare [**IMFASFProfile:: CreateMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createmutualexclusion) per creare un oggetto di esclusione reciproca vuota.
2.  Chiamare [**IMFASFMutualExclusion:: seTYPE**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-settype) per impostare il criterio del flusso che si escludono a vicenda.

    I flussi si escludono a vicenda in base a lingua, velocità in bit, presentazione e criteri personalizzati. Il tipo è rappresentato come GUID. Per un elenco di queste costanti, vedere [GUID del tipo di esclusione reciproca ASF](asf-mutual-exclusion-type-guids.md).

3.  Chiamare [**IMFASFMutualExclusion:: AddRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-addrecord) per aggiungere un record all'oggetto di esclusione reciproca.

    Questo metodo aggiunge un record vuoto e lo assegna a un indice di record a partire da zero.

4.  Chiamare [**IMFASFMutualExclusion:: AddStreamForRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-addstreamforrecord) per aggiungere il numero del flusso al record specificato dall'indice del record.

    Ogni record include uno o più flussi. Ogni flusso in un record si escludono a vicenda tutti i flussi in ogni altro record. Per ottenere il numero di flussi in un record, chiamare [**IMFASFMutualExclusion:: GetStreamsForRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getstreamsforrecord) specificando l'indice del record.

    Per rimuovere un flusso dal record, chiamare [**IMFASFMutualExclusion:: RemoveStreamFromRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-removestreamfromrecord) e specificare l'indice del record e il numero di flusso.

5.  Chiamare [**IMFASFProfile:: AddMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion) per aggiungere l'oggetto di esclusione reciproca configurato al profilo.

## <a name="enumerating-mutual-exclusion-objects-in-a-profile"></a>Enumerazione degli oggetti di esclusione reciproca in un profilo

Se [**IMFASFProfile:: AddMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion) ha esito positivo, assegna un indice all'oggetto specificato, a partire da zero.

Per enumerare gli oggetti di esclusione reciproca associati a un profilo, chiamare [**IMFASFProfile:: GetMutualExclusionCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusioncount) e scorrere l'elenco chiamando [**IMFASFProfile:: GetMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusion). Gli indici di esclusione reciproca sono sequenziali e variano da 0 a uno inferiore rispetto al numero di flussi recuperato da **GetMutualExclusionCount**.

Un oggetto di esclusione reciproca viene rimosso dal profilo chiamando [**IMFASFProfile:: RemoveMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removemutualexclusion). Il profilo riassegna gli indici di esclusione reciproca in modo che siano sequenziali a partire da zero. Questa operazione sovrascrive gli indici archiviati in precedenza, che non sono più validi dopo la chiamata a questo metodo. Questa operazione rilascia i record del flusso di esclusione reciproca associato.

## <a name="removing-records-in-a-mutual-exclusion-object"></a>Rimozione di record in un oggetto di esclusione reciproca

Per rimuovere un record da un oggetto di esclusione reciproca, chiamare [**IMFASFMutualExclusion:: RemoveRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-removerecord). Se questo metodo ha esito positivo, l'oggetto di esclusione reciproca indicizza i record rimanenti in modo che siano sequenziali a partire da zero. L'applicazione deve enumerare i record per garantire l'indice corretto per ogni record. A tale scopo, chiamare [**IMFASFMutualExclusion:: GetRecordCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getrecordcount) e scorrere i record chiamando [**IMFASFMutualExclusion:: GetStreamsForRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getstreamsforrecord).

La rimozione del record con l'indice più alto non ha alcun effetto sugli altri indici.

## <a name="modifying-a-mutual-exclusion-object"></a>Modifica di un oggetto di esclusione reciproca

Per modificare la configurazione dell'oggetto di esclusione reciproca nel profilo, l'applicazione deve sostituire l'oggetto di esclusione reciproca esistente con un altro oggetto che contiene le nuove impostazioni.

Per modificare la configurazione dell'oggetto di esclusione reciproca nel profilo

1.  Enumerare gli oggetti di esclusione reciproca nel profilo per ottenere l'oggetto che deve essere modificato.
2.  Chiamare [**IMFASFMutualExclusion:: Clone**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-clone) per clonare l'oggetto di esclusione reciproca.

3.  Configurare l'oggetto clonato come richiesto.
4.  Chiamare [**IMFASFProfile:: RemoveMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removemutualexclusion) per rimuovere l'oggetto di esclusione reciproca precedente dal profilo.

5.  Chiamare [**IMFASFProfile:: AddMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion) per aggiungere l'oggetto di esclusione reciproca aggiornata al profilo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Profilo ASF](asf-profile.md)
</dt> </dl>

 

 



