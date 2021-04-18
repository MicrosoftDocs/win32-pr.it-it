---
description: Il file VBScript WiLstPrd.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori. Lo script di esempio si connette a un oggetto del programma di installazione ed enumera i prodotti registrati e le informazioni sul prodotto.
ms.assetid: 13615dc2-ebc7-4536-9dd8-9bb1dbf3cfaf
title: Elencare prodotti, proprietà, funzionalità e componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20d2f563efad42108f763b909e7a1118e255dcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307247"
---
# <a name="list-products-properties-features-and-components"></a>Elencare prodotti, proprietà, funzionalità e componenti

Il file VBScript WiLstPrd.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md). Lo script di esempio si connette a un oggetto del [**programma di installazione**](installer-object.md) ed enumera i prodotti registrati e le informazioni sul prodotto.

Questo esempio illustra l'uso di:

-   [**Proprietà ProductInfo**](installer-productinfo.md)
-   [**Proprietà ProductState (oggetto Installer)**](installer-productstate-property.md)
-   [**Products (proprietà)**](installer-products.md)
-   [**Proprietà features**](installer-features.md)
-   [**Proprietà FeatureParent**](installer-featureparent.md)
-   [**Proprietà FeatureState**](installer-featurestate.md)
-   [**Components (proprietà)**](installer-components.md)
-   [**Proprietà ComponentClients**](installer-componentclients.md)
-   [**Proprietà ComponentPath**](installer-componentpath.md)
-   [**Metodo LastErrorRecord**](installer-lasterrorrecord.md)
-   [**Metodo RegistryValue**](installer-registryvalue.md) dell' [ **oggetto Installer**](installer-object.md)

Per usare questo esempio, è necessaria la versione CScript.exe o WScript.exe di Windows script host. Per utilizzare CScript.exe per eseguire questo esempio, digitare una riga di comando al prompt dei comandi utilizzando la sintassi seguente. La guida viene visualizzata se il primo argomento è/? oppure se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ percorso del file \] . Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se la guida viene richiamata e 2 se lo script ha esito negativo.

**opzioni cscript WiLstPrd.vbs \[ Product Name \] \[\]**

Specificare il nome prodotto senza distinzione tra maiuscole e minuscole o il GUID ID prodotto del prodotto installato o pubblicizzato. Se non viene specificato alcun prodotto o opzione, il programma di installazione elenca tutti i prodotti installati o annunciati nel sistema.

Si noti che queste opzioni non sono opzioni, pertanto non è necessario anteporre una barra (/) nella riga di comando. Le opzioni seguenti possono essere combinate concatenando le lettere. Ad esempio, "PC" per elencare le proprietà dei prodotti e i componenti installati.



| Opzione               | Descrizione                                                                                                                           |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Nessuna opzione specificata | Elenca le proprietà dei prodotti.                                                                                                        |
| p                    | Elenca le proprietà dei prodotti.                                                                                                        |
| f                    | Elencare le funzionalità e gli Stati di installazione dei prodotti                                                                 |
| c                    | Elenca i componenti installati dei prodotti.                                                                                              |
| d                    | Elencare il valore in **HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ SharedDLLs** per i file di chiave del componente Products. |



 

Per ulteriori informazioni, vedere [Windows Installer esempi di script](windows-installer-scripting-examples.md) per ulteriori esempi di scripting. Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).

 

 



