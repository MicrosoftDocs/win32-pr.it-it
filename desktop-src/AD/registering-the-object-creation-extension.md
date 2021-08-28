---
title: Registrazione dell'estensione per la creazione di oggetti
description: Quando viene creata una DLL di estensione per la creazione di oggetti in Active Directory Domain Services, è necessario registrarla con il Registro di sistema di Windows e Active Directory Domain Services per rendere com e gli snap-in MMC amministrativi di Active Directory in grado di riconoscere l'estensione.
ms.assetid: 6e950c6c-1a4f-4de0-9be1-004c31d4734c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d99e83d718f98255a3f06e1a8de1c09fb88ae8582c107fce70a6963bdf5c38b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184466"
---
# <a name="registering-the-object-creation-extension"></a>Registrazione dell'estensione per la creazione di oggetti

Quando viene creata una DLL di estensione per la creazione di oggetti in Active Directory Domain Services, è necessario registrarla con il Registro di sistema di Windows e Active Directory Domain Services per rendere com e gli snap-in MMC amministrativi di Active Directory in grado di riconoscere l'estensione.

## <a name="registering-in-the-windows-registry"></a>Registrazione nel Registro Windows dati

Come tutti i server COM, un'estensione per la creazione di oggetti deve essere registrata nel registro Windows sistema. L'estensione viene registrata nella chiave seguente:

```
HKEY_CLASSES_ROOT
   CLSID
      <extension CLSID>
         InProcServer32
            (Default) = <extension path>
            ThreadingModel = Apartment
```

" CLSID di estensione " è la rappresentazione di stringa &lt; &gt; del CLSID come prodotto dalla [**funzione StringFromCLSID.**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) " &lt; percorso &gt; dell'estensione " contiene il percorso e il nome file della DLL di estensione. Il **valore ThreadingModel** per tutte le estensioni per la creazione di oggetti deve essere "Apartment".

## <a name="registering-with-active-directory-domain-services"></a>Registrazione con Active Directory Domain Services

La registrazione dell'estensione per la creazione di oggetti è specifica di un'impostazione locale. Se l'estensione per la creazione di oggetti si applica a tutte le impostazioni locali, deve essere registrata nell'oggetto **displaySpecifier** della classe di oggetti in tutti i sottocontenitori delle impostazioni locali nel contenitore DisplaySpecifiers. Se l'estensione per la creazione di oggetti è localizzata per determinate impostazioni locali, registrarla nell'oggetto **displaySpecifier** nel sottocontenitore delle impostazioni locali. Per altre informazioni sul contenitore DisplaySpecifiers e sulle impostazioni locali, vedere [Identificatori](display-specifiers.md) di visualizzazione e [Contenitore DisplaySpecifiers](displayspecifiers-container.md).

Esistono due attributi DisplaySpecifier in cui è possibile registrare un'estensione per la creazione di oggetti. Si tratta **di creationWizard** e **createWizardExt.**

**L'attributo creationWizard** identifica le estensioni principali per la creazione di oggetti per sostituire la creazione guidata di oggetti esistenti o nativi negli snap-in amministrativi di Active Directory. Un'estensione per la creazione primaria fornisce il primo set di pagine ed è ospitata nello stesso modo delle pagine native. Questo attributo è a valore singolo e richiede il formato seguente:


```C++
<CLSID>
```



" CLSID " è la rappresentazione di stringa del &lt; &gt; CLSID dell'oggetto COM come prodotto dalla [**funzione StringFromCLSID.**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid)

**L'attributo createWizardExt** identifica le estensioni di creazione di oggetti secondari. Un'estensione per la creazione secondaria aggiunge pagine della procedura guidata alle pagine native o all'estensione primaria. Questo attributo è multivalore e richiede il formato seguente:


```C++
<order number>,<CLSID>
```



Il " &lt; numero di ordine " è un numero senza segno che rappresenta la posizione della pagina nella procedura &gt; guidata. Quando viene visualizzata una creazione guidata, i valori vengono ordinati usando un confronto del " numero di ordine" &lt; di ogni &gt; valore. Se più valori hanno lo stesso " numero di ordine ", tali pagine vengono caricate nell'ordine in cui vengono &lt; &gt; lette dal server Active Directory. Se possibile, è consigliabile usare un " numero di ordine " non esistente, ovvero uno che non è stato usato da altri &lt; &gt; valori nella proprietà . Non è stata specificata alcuna posizione iniziale e sono consentiti spazi nella sequenza " &lt; numero di &gt; ordine ".

" CLSID " è la rappresentazione di stringa del &lt; &gt; CLSID dell'oggetto COM come prodotto dalla [**funzione StringFromCLSID.**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid)

 

 