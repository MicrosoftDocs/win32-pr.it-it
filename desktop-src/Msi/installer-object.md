---
description: Un oggetto del programma di installazione deve essere inizialmente creato per caricare il supporto di automazione necessario per COM per accedere alle funzioni del programma di installazione. Questo oggetto fornisce i wrapper per creare gli oggetti di primo livello e accedere ai relativi metodi.
ms.assetid: fefc3e39-073e-4869-86b7-27d20a3b337b
title: Oggetto Installer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4afddcce55a739ad322be10c736a6e9119f5c9eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324614"
---
# <a name="installer-object"></a>Oggetto Installer

Un oggetto del **programma di installazione** deve essere inizialmente creato per caricare il supporto di automazione necessario per com per accedere alle funzioni del programma di installazione. Questo oggetto fornisce i wrapper per creare gli oggetti di primo livello e accedere ai relativi metodi.

È possibile creare l'oggetto del **programma di installazione** dal ProgID "WindowsInstaller. Installer".

## <a name="members"></a>Membri

L'oggetto del **programma di installazione** include i seguenti tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'oggetto del **programma di installazione** .



| Metodo                                                                   | Descrizione                                                                                                                                                                                     |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddSource**](installer-addsource.md)                                 | Aggiunge un'origine all'elenco di origini di rete valide nell'elenco di origine.<br/>                                                                                                                |
| [**AdvertiseProduct**](installer-advertiseproduct.md)                   | Annuncia un pacchetto di installazione.<br/>                                                                                                                                                  |
| [**AdvertiseScript**](installer-advertisescript.md)                     | Annuncia un pacchetto di installazione. <br/>                                                                                                                                                 |
| [**ApplyMultiplePatches**](installer-applymultiplepatches.md)           | Applica una o più patch ai prodotti idonei per la ricezione della patch. Imposta la proprietà [**patch**](patch.md) sul percorso dei pacchetti di patch forniti.<br/>                          |
| [**ApplyPatch**](installer-applypatch.md)                               | Richiama un'installazione e imposta la proprietà [**patch**](patch.md) sul percorso del pacchetto di patch per ogni prodotto elencato dal pacchetto di patch come idoneo per la ricezione della patch.<br/> |
| [**ClearSourceList**](installer-clearsourcelist.md)                     | Rimuove tutte le origini di rete dall'oggetto di origine.<br/>                                                                                                                                     |
| [**CollectUserInfo**](installer-collectuserinfo.md)                     | Richiama una sequenza guidata dell'interfaccia utente che raccoglie e archivia sia le informazioni utente che il codice del prodotto.<br/>                                                                        |
| [**ConfigureFeature**](installer-configurefeature.md)                   | Configura lo stato di installazione di una funzionalità del prodotto.<br/>                                                                                                                                 |
| [**ConfigureProduct**](installer-configureproduct.md)                   | Installa o Disinstalla un prodotto.<br/>                                                                                                                                                    |
| [**CreateAdvertiseScript**](installer-createadvertisescript.md)         | Genera uno script di annuncio.<br/>                                                                                                                                                       |
| [**CreaRecord**](installer-createrecord.md)                           | Restituisce un nuovo oggetto [**record**](record-object.md) con il numero di campi richiesto.<br/>                                                                                            |
| [**EnableLog**](installer-enablelog.md)                                 | Abilita la registrazione del tipo di messaggio selezionato per tutte le sessioni di installazione successive nello spazio di processo corrente.<br/>                                                                  |
| [**ExtractPatchXMLData**](installer-extractpatchxmldata.md)             | Estrae le informazioni da una patch come stringa XML.<br/>                                                                                                                                  |
| [**FileHash**](installer-filehash.md)                                   | Accetta il percorso di un file e restituisce un hash a 128 bit del file.<br/>                                                                                                                    |
| [**FileSignatureInfo**](installer-filesignatureinfo.md)                 | Accetta il percorso di un file e restituisce un **SAFEARRAY** di byte che rappresenta l'hash o il certificato codificato.<br/>                                                                   |
| [**FileSize**](installer-filesize.md)                                   | Restituisce la dimensione del file specificato.<br/>                                                                                                                                              |
| [**FileVersion**](installer-fileversion.md)                             | Restituisce la stringa di versione o la stringa della lingua del percorso specificato.<br/>                                                                                                                 |
| [**ForceSourceListResolution**](installer-forcesourcelistresolution.md) | Impone al programma di installazione di eseguire la ricerca nell'elenco di origine di una fonte di prodotto valida la volta successiva che è necessaria un'origine.<br/>                                                                        |
| [**InstallProduct**](installer-installproduct.md)                       | Apre un pacchetto di installazione e Inizializza una sessione di installazione.<br/>                                                                                                                  |
| [**LastErrorRecord**](installer-lasterrorrecord.md)                     | Restituisce un oggetto [**record**](record-object.md) che contiene i parametri di errore per l'errore più recente della funzione che ha prodotto il record di errore.<br/>                          |
| [**OpenDatabase**](installer-opendatabase.md)                           | Apre un database esistente o ne crea uno nuovo.<br/>                                                                                                                                     |
| [**OpenPackage**](installer-openpackage.md)                             | Apre un pacchetto di installazione da usare con funzioni che accedono al database del prodotto e installano il motore.<br/>                                                                               |
| [**OpenProduct**](installer-openproduct.md)                             | Apre un pacchetto di installazione per un prodotto installato utilizzando il codice prodotto.<br/>                                                                                                          |
| [**ProvideAssembly**](installer-provideassembly.md)                     | Restituisce il percorso installato di un assembly.<br/>                                                                                                                                           |
| [**ProvideComponent**](installer-providecomponent.md)                   | Restituisce il percorso completo del componente ed esegue le installazioni necessarie.<br/>                                                                                                             |
| [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) | Restituisce il percorso completo del componente ed esegue le installazioni necessarie.<br/>                                                                                                             |
| [**RegistryValue**](installer-registryvalue.md)                         | Legge le informazioni relative a una chiave del registro di sistema specificata.<br/>                                                                                                                           |
| [**ReinstallFeature**](installer-reinstallfeature.md)                   | Reinstalla le funzionalità o corregge i problemi con le funzionalità installate.<br/>                                                                                                                    |
| [**ReinstallProduct**](installer-reinstallproduct.md)                   | Reinstalla un prodotto o corregge i problemi di installazione in un prodotto installato.<br/>                                                                                                      |
| [**RemovePatches**](installer-removepatches.md)                         | Rimuove una o più patch ai prodotti idonei per la ricezione della patch. <br/>                                                                                                              |
| [**UseFeature**](installer-usefeature.md)                               | Incrementa il conteggio di utilizzo per una particolare funzionalità e restituisce lo stato di installazione per tale funzionalità.<br/>                                                                             |



 

### <a name="properties"></a>Proprietà

L'oggetto del **programma di installazione** dispone di queste proprietà.



| Proprietà                                                                    | Tipo di accesso           | Descrizione                                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClientsEx**](installer-components.md)<br/>                        |                       | Restituisce un [**oggetto elenco che**](recordlist-object.md) elenca i prodotti che utilizzano un componente installato specificato.<br/> **[Windows Installer 4,5 e versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato.<br/>       |
| [**ComponentClients**](installer-componentclients.md)<br/>           |                       | Restituisce un oggetto [**String**](stringlist-object.md) enumeratore che enumera il set di client di un componente specificato.<br/>                                                                                                                           |
| [**ComponentPath**](installer-componentpath.md)<br/>                 |                       | Restituisce il percorso completo di un componente installato.<br/>                                                                                                                                                                                            |
| [**ComponentPathEx**](installer-componentpathex.md)<br/>             |                       | Restituisce un oggetto di [**record**](recordlist-object.md) che fornisce il percorso completo di un componente installato specificato. <br/> **[Windows Installer 4,5 e versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato.<br/>       |
| [**ComponentQualifiers**](installer-componentqualifiers.md)<br/>     |                       | Restituisce un oggetto [**String**](stringlist-object.md) enumeratore che enumera il set di qualificatori registrati per il componente specificato.<br/>                                                                                                          |
| [**Componenti**](installer-components.md)<br/>                       |                       | Restituisce un oggetto [**String**](stringlist-object.md) enumerando il set di componenti installati per tutti i prodotti.<br/>                                                                                                                      |
| [**ComponentsEx**](installer-componentsex.md)<br/>                   |                       | Restituisce un [**oggetto elenco che**](recordlist-object.md) elenca i componenti installati.<br/> **[Windows Installer 4,5 e versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato.<br/>                                    |
| [**Ambiente**](installer-environment.md)<br/>                     | Lettura/Scrittura<br/> | Valore stringa per una variabile di ambiente del processo corrente.<br/>                                                                                                                                                                        |
| [**FeatureParent**](installer-featureparent.md)<br/>                 |                       | Specifica la funzionalità padre di una funzionalità.<br/>                                                                                                                                                                                                  |
| [**Funzionalità**](installer-features.md)<br/>                           |                       | Restituisce un oggetto [**String**](stringlist-object.md) che enumera il set di funzionalità pubblicate per il prodotto specificato.<br/>                                                                                                               |
| [**FeatureState**](installer-featurestate.md)<br/>                   |                       | Restituisce lo stato di installazione di una funzionalità.<br/>                                                                                                                                                                                                   |
| [**FeatureUsageCount**](installer-featureusagecount.md)<br/>         |                       | Restituisce il numero di volte in cui la funzionalità è stata utilizzata.<br/>                                                                                                                                                                                 |
| [**FeatureUsageDate**](installer-featureusagedate.md)<br/>           |                       | Restituisce la data dell'ultima utilizzo della funzionalità specificata.<br/>                                                                                                                                                                                  |
| [**FileAttributes**](installer-fileattributes.md)<br/>               |                       | Restituisce un numero che rappresenta gli attributi di file combinati per il percorso designato di un file o di una cartella.<br/>                                                                                                                                  |
| [**Patch**](installer-patches.md)<br/>                             |                       | Restituisce un oggetto [**String**](stringlist-object.md) che contiene tutte le patch applicate al prodotto.<br/>                                                                                                                              |
| [**PatchesEx**](installer-patchesex.md)<br/>                         |                       | Enumera una raccolta di oggetti [**patch**](patch-object.md) .<br/>                                                                                                                                                                           |
| [**PatchFiles**](installer-patchfiles.md)<br/>                       |                       | Restituisce un oggetto [**String**](stringlist-object.md) List contenente un elenco di file che possono essere aggiornati dall'elenco di patch fornito.<br/>                                                                                                 |
| [**PatchInfo**](installer-patchinfo.md)<br/>                         |                       | Restituisce informazioni su una patch.<br/>                                                                                                                                                                                                          |
| [**PatchTransforms**](installer-patchtransforms.md)<br/>             |                       | Restituisce l'elenco delimitato da punti e virgola delle trasformazioni presenti nel pacchetto di patch specificato e applicate al prodotto specificato.<br/>                                                                                                            |
| [**ProductElevated**](installer-productelevated.md)<br/>             |                       | Restituisce true se il prodotto è gestito o false se il prodotto non è gestito.<br/>                                                                                                                                                              |
| [**ProductInfo**](installer-productinfo.md)<br/>                     |                       | Restituisce il valore dell'attributo specificato per un prodotto installato o pubblicato.<br/>                                                                                                                                                         |
| [**ProductInfoFromScript**](installer-productinfofromscript.md)<br/> |                       | Restituisce il valore dell'attributo specificato archiviato in uno script di annuncio.<br/>                                                                                                                                                         |
| [**Prodotti**](installer-products.md)<br/>                           |                       | Restituisce un oggetto [**String**](stringlist-object.md) enumerando il set di tutti i prodotti installati o annunciati per l'utente e il computer correnti. <br/>                                                                                     |
| [**ProductsEx**](installer-productsex.md)<br/>                       |                       | Enumera una raccolta di oggetti [**Product**](product-object.md) .<br/>                                                                                                                                                                       |
| [**ProductState**](installer-productstate-property.md)<br/>          |                       | Restituisce le informazioni sullo stato di installazione di un prodotto.<br/>                                                                                                                                                                                        |
| [**QualifierDescription**](installer-qualifierdescription.md)<br/>   |                       | Restituisce una stringa di testo che descrive il componente completo.<br/>                                                                                                                                                                               |
| [**RelatedProducts**](installer-relatedproducts.md)<br/>             |                       | Restituisce un oggetto [**String**](stringlist-object.md) che enumera il set di tutti i prodotti installati o annunciati per l'utente e il computer correnti con una proprietà [**UpgradeCode**](upgradecode.md) specificata nella tabella delle proprietà.<br/> |
| [**ShortcutTarget**](installer-shortcuttarget.md)<br/>               |                       | Esamina un collegamento e ne restituisce il prodotto, il nome della funzionalità e il componente, se disponibile.<br/>                                                                                                                                                       |
| [**SummaryInformation**](installer-summaryinformation.md)<br/>       |                       | Restituisce un oggetto [**SummaryInfo**](summaryinfo-object.md) che può essere utilizzato per esaminare, aggiornare e aggiungere proprietà al flusso di informazioni di riepilogo di un pacchetto o di una trasformazione.<br/>                                                              |
| [**UILevel**](installer-uilevel.md)<br/>                             | Lettura/Scrittura<br/> | Indica il tipo di interfaccia utente da utilizzare per l'apertura e l'elaborazione di pacchetti successivi nello spazio di processo corrente.<br/>                                                                                                           |
| [**Versione**](installer-version.md)<br/>                             |                       | Restituisce la rappresentazione di stringa della versione corrente di Windows Installer.<br/>                                                                                                                                                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso dell'interfaccia di automazione](using-the-automation-interface.md)
</dt> <dt>

[Esempi di script di Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




