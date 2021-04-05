---
title: Estensione dell'interfaccia utente per le nuove classi di oggetti
description: Active Directory Domain Services e la relativa interfaccia utente snap-in MMC amministrativa possono essere personalizzate per adattarsi ai requisiti di amministratori e utenti.
ms.assetid: 38e3b800-20ad-4da8-ad40-4e90838acfb5
ms.tgt_platform: multiple
keywords:
- Estensione dell'interfaccia utente per le nuove classi di oggetti AD
- Oggetto AD, estensione dell'interfaccia utente per le nuove classi di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 154b64a23eff72bf5751085a8e50691cd222abd6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955127"
---
# <a name="user-interface-extension-for-new-object-classes"></a>Estensione dell'interfaccia utente per le nuove classi di oggetti

Active Directory Domain Services e la relativa interfaccia utente snap-in MMC amministrativa possono essere personalizzate per adattarsi ai requisiti di amministratori e utenti. Active Directory Domain Services abilitare la modifica dello schema creando nuove classi e attributi o modificando le classi esistenti. Gli identificatori di visualizzazione per le classi possono essere modificati in modo da riflettere i nuovi elementi dell'interfaccia utente necessari per le modifiche dello schema.

Nella tabella seguente sono elencati gli attributi che possono essere utilizzati per modificare la modalità di visualizzazione degli oggetti di una determinata classe da parte degli snap-in amministrazione.



| Attributo                  | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **defaultHidingValue**     | L'attributo **defaultHidingValue** è un attributo di un oggetto **classSchema** . Questo attributo contiene un valore booleano che, se impostato su TRUE, fa sì che le istanze della classe di oggetti siano nascoste negli snap-in amministrativi e nella shell di Windows. Ciò significa anche che una voce di menu per la nuova classe di oggetti non viene visualizzata nel **nuovo** menu di scelta rapida degli snap-in di amministrazione, anche se le proprietà appropriate della creazione guidata sono impostate per l'oggetto **displaySpecifier** della nuova classe di oggetti. Se questo attributo è FALSE, le istanze della classe saranno visibili negli snap-in amministrativi e nella shell. Inoltre, una voce di menu Crea una nuova istanza dell'oggetto da aggiungere al **nuovo** menu degli snap-in amministrativi.<br/> Se per questo attributo non è impostato alcun valore, il valore predefinito è TRUE. Ciò significa che, per impostazione predefinita, le istanze dell'oggetto sono nascoste.<br/>                                                                |
| **showInAdvancedViewOnly** | L'attributo **showInAdvancedViewOnly** contiene un valore booleano che, se impostato su true, fa sì che le istanze della classe di oggetti vengano visualizzate nello snap-in utenti e computer nella visualizzazione avanzata e non vengano visualizzate nella shell di Windows. Se questa proprietà è FALSE, le istanze della classe saranno visibili in visualizzazione normale nello snap-in utenti e computer e nella shell di Windows.<br/> Se per questo attributo non è impostato alcun valore, il valore predefinito è TRUE.<br/> Questo attributo può essere impostato su un singolo oggetto per eseguire l'override del valore impostato sulla classe di oggetti. Ad esempio, la classe **contenitore** ha questo attributo impostato su true, ma il valore del contenitore **utente** è impostato su false. Per questo motivo, il contenitore **utente** viene visualizzato nella shell e in visualizzazione normale nello snap-in utenti e computer ma altri contenitori che non dispongono di **SHOWINADVANCEDVIEWONLY** impostato su false vengono visualizzati solo nella visualizzazione avanzata nello snap-in utenti e computer.<br/> |



 

## <a name="creating-display-specifiers-for-new-classes"></a>Creazione di identificatori di visualizzazione per le nuove classi

Per personalizzare l'interfaccia utente per una nuova classe, creare un oggetto identificatore di visualizzazione per la nuova classe per ogni impostazione locale supportata, quindi impostare gli attributi desiderati per l'identificatore di visualizzazione.

## <a name="inheriting-display-specifiers-for-derived-classes"></a>Ereditarietà degli identificatori di visualizzazione per le classi derivate

Una nuova classe che eredita da una classe esistente non eredita l'identificatore di visualizzazione della classe padre. Se la nuova classe utilizza alcune o tutte le proprietà dell'identificatore di visualizzazione della classe padre, creare un nuovo identificatore di visualizzazione per la nuova classe e copiare le proprietà dall'identificatore di visualizzazione della classe padre nel nuovo identificatore di visualizzazione dell'oggetto. Questa operazione deve essere eseguita per tutte le impostazioni locali per le quali vengono applicate le proprietà dell'identificatore di visualizzazione della classe padre.

Alcune parti del set di funzionalità dell'interfaccia utente, ad esempio le voci di menu e la creazione guidata per la classe utente, vengono implementate internamente e non sono disponibili per l'utilizzo da parte di un oggetto derivato. In questi casi è preferibile estendere una classe esistente rispetto all'uso di una classe derivata.

## <a name="modifying-existing-classes"></a>Modifica di classi esistenti

È possibile aggiungere nuovi attributi a una classe esistente. È possibile aggiungere nuovi componenti dell'interfaccia utente (pagine delle proprietà, voci di menu e nomi visualizzati degli attributi) o sostituire l'interfaccia utente esistente. È anche possibile progettare nuove pagine delle proprietà che espongono un minor numero di attributi di una classe e per creare menu di scelta rapida con meno azioni. Per altre informazioni, vedere [pagine delle proprietà da usare con gli identificatori di visualizzazione](property-pages-for-use-with-display-specifiers.md), i [menu di scelta rapida da usare con gli identificatori di visualizzazione](context-menus-for-use-with-display-specifiers.md)e [i nomi visualizzati delle classi e degli attributi](class-and-attribute-display-names.md).

 

 





