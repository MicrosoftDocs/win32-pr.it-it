---
title: Profiles
description: Profiles
ms.assetid: 6e70393f-3dab-4036-8d34-a672ef1795c6
keywords:
- Windows Media Format SDK, profili
- Advanced Systems Format (ASF), profiles
- ASF (Advanced Systems Format),profiles
- Windows File media format SDK,.prx
- File ASF (Advanced Systems Format), prx
- FILE ASF (Advanced Systems Format), file con estensione prx
- Windows Media Format SDK, Editor profili
- Advanced Systems Format (ASF), Editor profili
- ASF (Advanced Systems Format), Editor profili
- File con estensione prx
- file prx
- Editor profili
- Windows Codificatore multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64a89c06f031c9cf8214888efb35f2986135f88207fc94a631e1e111c94ce16d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707416"
---
# <a name="profiles"></a>Profiles

Un profilo è una raccolta di dati che descrive la configurazione di un file ASF. Un profilo deve contenere almeno le impostazioni di configurazione per un singolo flusso.

Le informazioni sul flusso in un profilo contengono la velocità in bit, la finestra del buffer e le proprietà multimediali per il flusso. Le informazioni di flusso per audio e video descrivono esattamente come viene configurato il supporto nel file, incluso il codec (se presente) che verrà usato per comprimere i dati.

Un profilo contiene anche informazioni sulle varie funzionalità dei file ASF che verranno usate nei file creati con esso. tra cui [l'esclusione reciproca,](mutual-exclusion.md) [la priorità del flusso,](stream-prioritization.md) [la condivisione della larghezza di banda](bandwidth-sharing.md)e le estensioni [unità dati.](data-unit-extensions.md)

Le versioni precedenti di Windows Media Format SDK hanno fornito profili di sistema preconfigurati, che possono essere usati per creare tipi comuni di file o modificati leggermente in base alle esigenze dell'applicazione. I profili di sistema non sono supportati per i codec Windows Media 9 Series. Questo perché il numero di tipi di file "comuni" è aumentato in modo esponenziale con l'aggiunta di nuove funzionalità. È previsto che praticamente ogni autore di contenuto abbia esigenze che vanno oltre le semplici soluzioni fornite dai profili di sistema. È comunque possibile usare i profili di sistema vecchi come punto di partenza. Per altre informazioni, vedere [Uso dei profili di sistema](using-system-profiles.md).

È necessario fornire al writer un profilo per ogni file scritto. È possibile specificare un profilo da usare con il writer chiamando [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).

I dati del profilo sono disponibili in diversi moduli che possono essere usati da Windows Media Format SDK. È anche possibile accedere alle informazioni del profilo in diversi modi. Ciò può causare confusione su che cos'è un profilo e su come viene usato.

Il diagramma seguente illustra come vengono usati i dati del profilo nell'SDK.

![diagramma che mostra il flusso di informazioni sul profilo.](images/formatsdk01.png)

I dati del profilo hanno tre forme diverse: i dati contenuti in un oggetto profilo in un'applicazione, un file XML su disco e i dati nell'intestazione di un file ASF. Ognuna di queste forme di dati viene visualizzata come rettangolo ombreggiato nel diagramma.

## <a name="data-in-a-profile-object"></a>Dati in un oggetto profilo

Quando si modifica un profilo, si usa un oggetto profilo che incapsula tutti i dati del profilo. È possibile creare un oggetto profilo vuoto usando l'oggetto di gestione del profilo. È anche possibile usare l'oggetto di gestione dei profili per caricare i dati del profilo esistenti in un oggetto profilo.

La maggior parte dei dati del profilo deve essere aggiunta e manipolata tramite l'uso di oggetti che rappresentano singole parti del profilo. Sono inclusi gli oggetti di configurazione del flusso, gli oggetti di esclusione reciproca, gli oggetti di condivisione della larghezza di banda e un oggetto di priorità del flusso. Ognuno di questi tipi di oggetto può essere creato usando i metodi nell'oggetto profilo. Le modifiche apportate a questi oggetti non influiscono sull'oggetto profilo finché non si usa un metodo nell'oggetto profilo per includere i dati aggiornati dall'altro oggetto.

## <a name="data-in-an-xml-file"></a>Dati in un file XML

I dati del profilo vengono archiviati su disco sotto forma di file XML con estensione prx. Incluso in Windows Media Format SDK è una raccolta di profili denominati profili di sistema che coprono i tipi più comuni di file ASF. I profili di sistema vengono archiviati in un file denominato WMSysPr9.prx. Si noti che questo file in realtà non contiene profili di sistema per Windows Media 9 Series perché il concetto di profili di sistema non è più usato. Quando si salvano profili personalizzati, è necessario salvarli nei propri file.

È possibile usare l'oggetto di gestione dei profili per salvare i dati da un oggetto profilo in una stringa di testo XML. È quindi possibile usare le funzioni di I/O di file che si desidera salvare la stringa in un file su disco.

## <a name="data-in-the-header-of-an-asf-file"></a>Dati nell'intestazione di un file ASF

Il writer accetta le informazioni dal profilo e le usa per creare i flussi che passano alla sezione dei dati del file ASF. La maggior parte dei dati del profilo viene archiviata nella sezione di intestazione del file quando viene scritto un file. Durante la riproduzione, l'oggetto lettore (o l'oggetto lettore sincrono) può accedere alle informazioni nell'intestazione del file. In questo caso, l'oggetto di lettura crea un oggetto profilo e lo popola con i dati dell'intestazione.

Quando si accede ai dati del profilo usando il lettore (o lettore sincrono), è possibile apportare modifiche alle informazioni del profilo, ma non è possibile applicare tali modifiche al file nel lettore. È possibile applicare le informazioni del profilo da un file in un lettore a un profilo in un writer per creare un nuovo file con le stesse impostazioni del file nel lettore. In questo caso, qualsiasi modifica apportata alle informazioni del profilo prima di impostare il profilo nel writer verrà riflessa nelle informazioni del profilo registrate dal writer.

## <a name="using-profile-editor"></a>Uso dell'editor di profili

Anziché creare profili usando Windows Media Format SDK, è possibile usare l'editor di profili, un'utilità inclusa in Windows Media Encoder. Nell'applicazione di codifica usare il **metodo IWMProfileManager::LoadProfileByData** per caricare il profilo salvato. In alcuni scenari, ad esempio se si usa un numero limitato di profili che non vengono mai modificati dinamicamente, potrebbe essere più comodo usare l'editor di profili per creare i profili.

Tuttavia, se si usa l'editor di profili, è consigliabile non usare l'impostazione "Dimensioni video: uguale a input video". Quando questa casella di controllo è selezionata, Editor profili creerà un profilo con l'altezza e la larghezza dell'output video impostate su zero. Quando Windows Media Encoder rileva questi profili, imposta i valori corretti in modo che corrispondano al relativo input video. Tuttavia, writer in Windows Media Format SDK non esegue questa operazione automaticamente, pertanto è necessario assicurarsi che l'applicazione imposta le dimensioni dei fotogrammi video nei casi in cui il profilo non ne abbia nessuno.

**Nota** Alcuni elementi di configurazione del flusso non vengono archiviati nel profilo. I dati nel profilo descrivono il formato del file ASF completato. Le proprietà dei supporti di input e altri dati di configurazione usati dall'oggetto writer per configurare i codec non vengono salvati nel profilo. Sono incluse tutte le proprietà impostate tramite il [**metodo IWMPropertyVault::SetProperty.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetto di condivisione della larghezza di banda**](bandwidth-sharing-object.md)
</dt> <dt>

[**Concetti**](concepts.md)
</dt> <dt>

[**Interfaccia IWMProfile**](iwmprofile.md)
</dt> <dt>

[**Interfaccia IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**Oggetto di esclusione reciproca**](mutual-exclusion-object.md)
</dt> <dt>

[**Oggetto Gestione profili**](profile-manager-object.md)
</dt> <dt>

[**Oggetto configurazione del flusso**](stream-configuration-object.md)
</dt> <dt>

[**Oggetto di definizione delle priorità dei flussi**](stream-prioritization-object.md)
</dt> <dt>

[**Uso dei profili**](working-with-profiles.md)
</dt> </dl>

 

 




