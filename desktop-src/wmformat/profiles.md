---
title: Profiles
description: Profiles
ms.assetid: 6e70393f-3dab-4036-8d34-a672ef1795c6
keywords:
- Windows Media Format SDK, profili
- ASF (Advanced Systems Format), profili
- ASF (formato avanzato dei sistemi), profili
- Windows Media Format SDK, file con estensione prx
- ASF (Advanced Systems Format), file con estensione prx
- ASF (Advanced Systems Format), file con estensione prx
- Windows Media Format SDK, Editor profili
- ASF (Advanced Systems Format), Editor profili
- ASF (formato avanzato dei sistemi), Editor profili
- file con estensione prx
- file PRX
- Editor profili
- Codificatore Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de244445a7c1301c7a14ef273b81ac9fd9cbfb62
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299421"
---
# <a name="profiles"></a>Profiles

Un profilo è una raccolta di dati che descrive la configurazione di un file ASF. Come minimo, un profilo deve contenere le impostazioni di configurazione per un singolo flusso.

Le informazioni sul flusso in un profilo contengono la velocità in bit, la finestra del buffer e le proprietà dei supporti per il flusso. Le informazioni sul flusso per audio e video descrivono esattamente il modo in cui il supporto viene configurato nel file, incluso il codec (se presente) che verrà usato per comprimere i dati.

Un profilo contiene inoltre informazioni sulle diverse funzionalità dei file ASF che verranno utilizzate nei file creati con esso. Sono inclusi l' [esclusione reciproca](mutual-exclusion.md), la [definizione delle priorità dei flussi](stream-prioritization.md), la condivisione della larghezza di [banda](bandwidth-sharing.md)e le estensioni delle [unità](data-unit-extensions.md)

Le versioni precedenti di Windows Media Format SDK fornivano profili di sistema preconfigurati, che potevano essere usati per creare tipi comuni di file o modificati leggermente per soddisfare le esigenze dell'applicazione. I profili di sistema non sono supportati per i codec della serie Windows Media 9. Questo è dovuto al fatto che il numero di tipi di file "comuni" è aumentato in modo esponenziale con l'aggiunta di nuove funzionalità. Si prevede che praticamente ogni autore di contenuti debba superare le semplici soluzioni fornite dai profili di sistema. È comunque possibile usare i vecchi profili di sistema come punto di partenza. Per ulteriori informazioni, vedere [using System Profiles](using-system-profiles.md).

È necessario fornire al writer un profilo per ogni file scritto. È possibile specificare un profilo da usare con il writer chiamando [**IWMWriter:: seprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).

I dati del profilo esistono in diversi formati che possono essere usati da Windows Media Format SDK. È anche possibile accedere alle informazioni sul profilo in diversi modi. Ciò può comportare confusione riguardo a un profilo e al modo in cui viene usato.

Il diagramma seguente illustra il modo in cui i dati di profilo vengono usati nell'SDK.

![diagramma che mostra il flusso delle informazioni sul profilo.](images/formatsdk01.png)

I dati del profilo assumono tre forme diverse: i dati contenuti in un oggetto profilo in un'applicazione, un file XML su disco e i dati nell'intestazione di un file ASF. Ognuno di questi tipi di dati viene visualizzato come rettangolo ombreggiato nel diagramma.

## <a name="data-in-a-profile-object"></a>Dati in un oggetto profilo

Quando si modifica un profilo, si utilizza un oggetto profilo, che incapsula tutti i dati del profilo. È possibile creare un oggetto profilo vuoto utilizzando l'oggetto Gestione profili. È anche possibile usare l'oggetto Gestione profili per caricare i dati di profilo esistenti in un oggetto profilo.

È necessario aggiungere e modificare la maggior parte dei dati del profilo tramite l'utilizzo di oggetti che rappresentano singole parti del profilo. Sono inclusi oggetti di configurazione del flusso, oggetti di esclusione reciproca, oggetti di condivisione della larghezza di banda e un oggetto di assegnazione di priorità del flusso Ognuno di questi tipi di oggetti può essere creato utilizzando i metodi nell'oggetto profilo. Apportare modifiche a questi oggetti non influisce sull'oggetto profilo fino a quando non si utilizza un metodo nell'oggetto profilo per includere i dati aggiornati dall'altro oggetto.

## <a name="data-in-an-xml-file"></a>Dati in un file XML

I dati del profilo vengono archiviati su disco sotto forma di file XML con estensione prx. Incluso in Windows Media Format SDK è una raccolta di profili denominati profili di sistema che coprono i tipi più comuni di file ASF. I profili di sistema vengono archiviati in un file denominato WMSysPr9. prx. Si noti che questo file non contiene alcun profilo di sistema per la serie Windows Media 9 perché il concetto di profili di sistema non viene più utilizzato. Quando si salvano i profili personalizzati, è necessario salvarli nei propri file.

È possibile utilizzare l'oggetto Gestione profili per salvare i dati da un oggetto profilo a una stringa di testo XML. È quindi possibile usare le funzioni di I/O dei file desiderate per salvare la stringa in un file su disco.

## <a name="data-in-the-header-of-an-asf-file"></a>Dati nell'intestazione di un file ASF

Il writer acquisisce le informazioni dal profilo e le usa per creare i flussi che vengono inseriti nella sezione dati del file ASF. Quando viene scritto un file, la maggior parte dei dati del profilo viene archiviata nella sezione dell'intestazione del file. Al momento della riproduzione, l'oggetto Reader (o l'oggetto Reader sincrono) può accedere alle informazioni nell'intestazione del file. In questo caso, l'oggetto di lettura crea un oggetto profilo e lo popola con i dati dell'intestazione.

Quando si accede ai dati del profilo utilizzando il lettore (o il lettore sincrono), è possibile apportare modifiche alle informazioni del profilo, ma non è possibile applicare tali modifiche al file nel lettore. È possibile applicare le informazioni sul profilo da un file in un lettore a un profilo in un writer per creare un nuovo file con le stesse impostazioni del file nel lettore. In questo caso, le modifiche apportate alle informazioni sul profilo prima di impostare il profilo nel writer verranno riflesse nelle informazioni sul profilo registrate dal writer.

## <a name="using-profile-editor"></a>Uso dell'Editor profili

Anziché creare profili usando Windows Media Format SDK, è possibile usare l'Editor profili, un'utilità inclusa in Windows Media Encoder. Nell'applicazione di codifica usare il metodo **IWMProfileManager:: LoadProfileByData** per caricare il profilo salvato. In alcuni scenari, ad esempio se si usa un numero limitato di profili che non vengono mai modificati dinamicamente, potrebbe essere più pratico usare l'Editor profili per creare i profili.

Tuttavia, se si usa l'Editor profili, è consigliabile non usare l'impostazione "dimensioni video: uguale a input video". Se questa casella di controllo è selezionata, l'Editor profili creerà un profilo con l'altezza e la larghezza dell'output del video impostate su zero. Quando il codificatore Windows Media rileva questi profili, imposta i valori corretti in modo che corrispondano al relativo input video. Tuttavia, il writer in Windows Media Format SDK non esegue questa operazione automaticamente, pertanto è necessario assicurarsi che l'applicazione imposti le dimensioni del fotogramma video nei casi in cui il profilo non sia presente.

**Nota** Alcuni elementi di configurazione del flusso non vengono archiviati nel profilo. Nei dati del profilo viene descritto il formato del file ASF completato. Le proprietà dei supporti di input e altri dati di configurazione usati dall'oggetto writer per configurare i codec non vengono salvati nel profilo. Sono incluse tutte le proprietà impostate tramite il metodo [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) .

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

[**Oggetto di assegnazione di priorità del flusso**](stream-prioritization-object.md)
</dt> <dt>

[**Utilizzo dei profili**](working-with-profiles.md)
</dt> </dl>

 

 




