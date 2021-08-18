---
description: Il file VBScript WiLstPrd.vbs disponibile in Windows SDK Components for Windows Installer Developers. Lo script di esempio si connette a un oggetto Installer ed enumera i prodotti registrati e le informazioni sui prodotti.
ms.assetid: 13615dc2-ebc7-4536-9dd8-9bb1dbf3cfaf
title: Elencare prodotti, proprietà, funzionalità e componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa090deef877757277b64cef02ecf42df61405fdc9238935bfffba756434f316
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013149"
---
# <a name="list-products-properties-features-and-components"></a>Elencare prodotti, proprietà, funzionalità e componenti

Il file VBScript WiLstPrd.vbs in Windows [SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md). Lo script di esempio si connette a un [**oggetto Installer**](installer-object.md) ed enumera i prodotti registrati e le informazioni sui prodotti.

In questo esempio viene illustrato l'uso di:

-   [**ProductInfo - proprietà**](installer-productinfo.md)
-   [**Proprietà ProductState (oggetto Installer)**](installer-productstate-property.md)
-   [**Products - proprietà**](installer-products.md)
-   [**Proprietà Features**](installer-features.md)
-   [**Proprietà FeatureParent**](installer-featureparent.md)
-   [**FeatureState - proprietà**](installer-featurestate.md)
-   [**Components - proprietà**](installer-components.md)
-   [**ComponentClients - proprietà**](installer-componentclients.md)
-   [**ComponentPath - proprietà**](installer-componentpath.md)
-   [**Metodo LastErrorRecord**](installer-lasterrorrecord.md)
-   [**Metodo RegistryValue**](installer-registryvalue.md) [ **dell'oggetto Installer**](installer-object.md)

Per usare questo esempio, è CScript.exe o WScript.exe versione di Windows script host. Per usare CScript.exe eseguire questo esempio, digitare una riga di comando al prompt dei comandi usando la sintassi seguente. La Guida viene visualizzata se il primo argomento è /? o se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ percorso del file \] . Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se viene richiamata la Guida e 2 se lo script non riesce.

**cscript WiLstPrd.vbs \[ product \] \[ name options\]**

Specificare il nome del prodotto senza distinzione tra maiuscole e minuscole o il GUID dell'ID prodotto del prodotto installato o annunciato. Se non viene specificato alcun prodotto o opzione, il programma di installazione elenca tutti i prodotti installati o annunciati nel sistema.

Si noti che queste opzioni non sono opzioni, pertanto è consigliabile non anterle con una barra (/) nella riga di comando. Le opzioni seguenti possono essere combinate concatenando le lettere. Ad esempio, "pc" per elencare sia le proprietà dei prodotti che i componenti installati.



| Opzione               | Descrizione                                                                                                                           |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| nessuna opzione specificata | Elencare le proprietà dei prodotti.                                                                                                        |
| p                    | Elencare le proprietà dei prodotti.                                                                                                        |
| f                    | Elencare le funzionalità dei prodotti, gli elementi padre delle funzionalità e gli stati di installazione                                                                 |
| c                    | Elencare i componenti installati dei prodotti.                                                                                              |
| d                    | Elencare il valore in **HKLM \\ Software Microsoft Windows \\ \\ \\ CurrentVersion \\ SharedDlls** per i file chiave del componente dei prodotti. |



 

Per altre informazioni, vedere Esempi [Windows di scripting del](windows-installer-scripting-examples.md) programma di installazione per altri esempi di scripting. Per le utilità di esempio che non richiedono Windows Script Host, vedere Windows [Installer Development Tools](windows-installer-development-tools.md).

 

 



