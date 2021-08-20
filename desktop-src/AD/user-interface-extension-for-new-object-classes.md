---
title: Interfaccia utente per le nuove classi di oggetti
description: Active Directory Domain Services e la relativa interfaccia utente dello snap-in MMC amministrativo possono essere personalizzati per adattarsi ai requisiti di amministratori e utenti.
ms.assetid: 38e3b800-20ad-4da8-ad40-4e90838acfb5
ms.tgt_platform: multiple
keywords:
- Interfaccia utente estensione per le nuove classi di oggetti AD
- Object AD, estensione Interfaccia utente per le nuove classi di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dd2f703e22619c8c3738b51a7a1f1464ca7e7d86b655abccd4c26258ac85810
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182711"
---
# <a name="user-interface-extension-for-new-object-classes"></a>Interfaccia utente per le nuove classi di oggetti

Active Directory Domain Services e la relativa interfaccia utente dello snap-in MMC amministrativo possono essere personalizzati per adattarsi ai requisiti di amministratori e utenti. Active Directory Domain Services lo schema da modificare creando nuove classi e attributi o modificando le classi esistenti. Gli identificatori di visualizzazione per le classi possono essere modificati per riflettere i nuovi elementi dell'interfaccia utente richiesti dalle modifiche dello schema.

Nella tabella seguente sono elencati gli attributi che è possibile utilizzare per modificare la modalità di visualizzazione degli oggetti di una determinata classe da parte degli snap-in amministrativi.



| Attributo                  | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **defaultHidingValue**     | **L'attributo defaultHidingValue** è un attributo di un **oggetto classSchema.** Questo attributo contiene un valore booleano che, se TRUE, fa sì che le istanze della classe di oggetti siano nascoste negli snap-in amministrativi e nella shell Windows sistema. Ciò significa anche che una voce di menu per  la nuova classe di oggetti non viene visualizzata nel menu di scelta rapida Nuovo degli snap-in amministrativi, anche se le proprietà appropriate della creazione guidata sono impostate nell'oggetto **displaySpecifier** della nuova classe di oggetti. Se questo attributo è FALSE, le istanze della classe saranno visibili negli snap-in amministrativi e nella shell. Ciò fa sì che una voce di menu crei una nuova istanza dell'oggetto da aggiungere al menu **Nuovo** degli snap-in amministrativi.<br/> Se per questo attributo non è impostato alcun valore, il valore predefinito è TRUE. Ciò significa che, per impostazione predefinita, le istanze dell'oggetto sono nascoste.<br/>                                                                |
| **showInAdvancedViewOnly** | **L'attributo showInAdvancedViewOnly** contiene un valore booleano che, se TRUE, fa sì che le istanze della classe di oggetti vengano visualizzate nello snap-in Utenti e computer solo nella visualizzazione avanzata e non vengano visualizzate nella shell Windows. Se questa proprietà è FALSE, le istanze della classe saranno visibili nella visualizzazione Normale nello snap-in Utenti e computer e nella shell Windows.<br/> Se per questo attributo non è impostato alcun valore, il valore predefinito è TRUE.<br/> Questo attributo può essere impostato su un singolo oggetto per eseguire l'override del valore impostato nella classe di oggetti. Ad esempio, la **classe Container** ha questo attributo impostato su TRUE, ma il **contenitore User** ha questo valore impostato su FALSE. Per questo scopo, il contenitore User viene visualizzato nella shell e nella visualizzazione Normale nello snap-in Utenti e computer, ma altri contenitori per cui **showInAdvancedViewOnly** non è impostato su FALSE vengono visualizzati solo nella visualizzazione Avanzate dello snap-in Utenti e computer. <br/> |



 

## <a name="creating-display-specifiers-for-new-classes"></a>Creazione di identificatori di visualizzazione per nuove classi

Per personalizzare l'interfaccia utente per una nuova classe, creare un oggetto identificatore di visualizzazione per la nuova classe per ogni impostazione locale supportata, quindi impostare gli attributi desiderati per l'identificatore di visualizzazione.

## <a name="inheriting-display-specifiers-for-derived-classes"></a>Ereditarietà degli identificatori di visualizzazione per le classi derivate

Una nuova classe che eredita da una classe esistente non eredita l'identificatore di visualizzazione della classe padre. Se la nuova classe deve usare alcune o tutte le proprietà dell'identificatore di visualizzazione della classe padre, creare un nuovo identificatore di visualizzazione per la nuova classe e copiare le proprietà dall'identificatore di visualizzazione della classe padre al nuovo identificatore di visualizzazione dell'oggetto. Questa operazione deve essere eseguita per tutte le impostazioni locali a cui si applicano le proprietà dell'identificatore di visualizzazione della classe padre.

Alcune parti del set di funzionalità dell'interfaccia utente, ad esempio le voci di menu e la creazione guidata per la classe utente, vengono implementate internamente e non sono disponibili per l'uso da parte di un oggetto derivato. In questi casi è meglio estendere una classe esistente anziché usare una classe derivata.

## <a name="modifying-existing-classes"></a>Modifica di classi esistenti

È possibile aggiungere nuovi attributi a una classe esistente. È possibile aggiungere nuovi componenti dell'interfaccia utente (pagine delle proprietà, voci di menu e nomi visualizzati degli attributi) o sostituire l'interfaccia utente esistente. È anche possibile progettare nuove pagine delle proprietà che espongono meno attributi di una classe e creare menu di scelta rapida con un minor numero di azioni. Per altre informazioni, [vedere](property-pages-for-use-with-display-specifiers.md)Pagine delle proprietà per l'uso con identificatori di visualizzazione , [Menu](context-menus-for-use-with-display-specifiers.md)di scelta rapida da usare con identificatori di visualizzazione e Nomi visualizzati di classi [e attributi](class-and-attribute-display-names.md).

 

 





