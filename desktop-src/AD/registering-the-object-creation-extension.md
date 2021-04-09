---
title: Registrazione dell'estensione per la creazione di oggetti
description: Quando viene creata una DLL di estensione per la creazione di oggetti in Active Directory Domain Services, deve essere registrata nel registro di sistema di Windows e Active Directory Domain Services per rendere COM e gli snap-in di MMC amministrativi Active Directory a conoscenza dell'estensione.
ms.assetid: 6e950c6c-1a4f-4de0-9be1-004c31d4734c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c27d8e2a50c2340d678fd43e546d68525afbc8a7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103956306"
---
# <a name="registering-the-object-creation-extension"></a>Registrazione dell'estensione per la creazione di oggetti

Quando viene creata una DLL di estensione per la creazione di oggetti in Active Directory Domain Services, deve essere registrata nel registro di sistema di Windows e Active Directory Domain Services per rendere COM e gli snap-in di MMC amministrativi Active Directory a conoscenza dell'estensione.

## <a name="registering-in-the-windows-registry"></a>Registrazione nel registro di sistema di Windows

Come tutti i server COM, un'estensione per la creazione di oggetti deve essere registrata nel registro di sistema di Windows. L'estensione viene registrata con la chiave seguente:

```
HKEY_CLASSES_ROOT
   CLSID
      <extension CLSID>
         InProcServer32
            (Default) = <extension path>
            ThreadingModel = Apartment
```

" &lt; estensione CLSID &gt; " è la rappresentazione di stringa del CLSID come prodotto dalla funzione [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) . " &lt; percorso estensione &gt; " contiene il percorso e il nome file della DLL di estensione. Il valore **ThreadingModel** per tutte le estensioni per la creazione di oggetti deve essere "Apartment".

## <a name="registering-with-active-directory-domain-services"></a>Registrazione con Active Directory Domain Services

La registrazione dell'estensione per la creazione di oggetti è specifica di un'impostazione locale. Se l'estensione per la creazione di oggetti si applica a tutte le impostazioni locali, deve essere registrata nell'oggetto **displaySpecifier** della classe di oggetti in tutti i sottocontenitori delle impostazioni locali nel contenitore DisplaySpecifiers. Se l'estensione per la creazione di oggetti è localizzata per determinate impostazioni locali, registrarla nell'oggetto **displaySpecifier** del sottocontenitore delle impostazioni locali. Per altre informazioni sul contenitore e sulle impostazioni locali di DisplaySpecifiers, vedere [identificatori di visualizzazione](display-specifiers.md) e [contenitore DisplaySpecifiers](displayspecifiers-container.md).

Sono disponibili due attributi DisplaySpecifier in cui è possibile registrare un'estensione per la creazione di oggetti. Si tratta di **creationWizard** e **createWizardExt**.

L'attributo **creationWizard** identifica le estensioni per la creazione di oggetti primari per sostituire la creazione guidata oggetto esistente o nativa in Active Directory snap-in amministrativi. Un'estensione per la creazione primaria fornisce il primo set di pagine ed è ospitata in modo analogo alle pagine native. Questo attributo è a valore singolo e richiede il formato seguente:


```C++
<CLSID>
```



" &lt; CLSID &gt; " è la rappresentazione di stringa del CLSID dell'oggetto com come prodotto dalla funzione [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .

L'attributo **createWizardExt** identifica le estensioni per la creazione di oggetti secondari. Un'estensione per la creazione secondaria aggiunge le pagine della procedura guidata alle pagine native o all'estensione primaria. Questo attributo è multivalore e richiede il formato seguente:


```C++
<order number>,<CLSID>
```



Il " &lt; numero &gt; di ordine" è un numero senza segno che rappresenta la posizione della pagina nella procedura guidata. Quando viene visualizzata una procedura guidata di creazione, i valori vengono ordinati usando un confronto tra il " &lt; numero di ordine" di ogni valore &gt; . Se più di un valore ha lo stesso " &lt; numero &gt; di ordine", le pagine vengono caricate nell'ordine in cui vengono lette dal server Active Directory. Se possibile, è consigliabile usare un " &lt; numero di ordine" non esistente, &gt; ovvero uno che non è stato usato da altri valori nella proprietà. Non esiste una posizione di inizio prescritta e sono consentiti gap nella &lt; sequenza "Order Number &gt; ".

" &lt; CLSID &gt; " è la rappresentazione di stringa del CLSID dell'oggetto com come prodotto dalla funzione [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .

 

 