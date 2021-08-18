---
title: Risoluzione dei conflitti dei nomi di funzioni/proprietà nell'automazione nelle estensioni
description: In questo argomento\ 0034;object \ 0034; indica l'oggetto, nel suo complesso, come lo visualizza un client ADSI. Ad esempio, ADSI e tutte le relative estensioni.
ms.assetid: 76207326-879e-408b-8004-06d940401a41
ms.tgt_platform: multiple
keywords:
- Risoluzione dei conflitti tra funzioni e nomi di proprietà nell'automazione nelle estensioni
- estensioni ADSI, risoluzione dei conflitti tra funzioni e nomi di proprietà in Automazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53701c95672fe209cb57a15e3292e1269dc37e66e36f041110dd502f8a8a1486
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637541"
---
# <a name="resolution-of-functionproperty-name-conflicts-in-automation-in-extensions"></a>Risoluzione dei conflitti dei nomi di funzioni/proprietà nell'automazione nelle estensioni

In questo argomento "object" indica l'oggetto, nel suo complesso, come lo visualizza un client ADSI. Ad esempio, ADSI e tutte le relative estensioni.

## <a name="same-function-name-with-the-same-parameters"></a>Stesso nome di funzione con gli stessi parametri

Se due o più interfacce [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) doppie in un oggetto supportano una proprietà o un metodo con lo stesso nome, ad esempio **Func1,** la chiamata viene determinata usando i criteri seguenti. Se il client ha un puntatore a una delle interfacce duali che supportano un metodo denominato **Func1** e se l'ambiente di automazione supporta l'accesso vtable, **Func1** viene richiamato direttamente tramite l'accesso vtable ADSI.

Se una delle condizioni precedenti è false, [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) e [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) vengono chiamati per richiamare **Func1**.

Per altre informazioni e una breve spiegazione su come un client può aggiungere un puntatore a un'interfaccia duale e una descrizione dei tipi di ambienti che supportano l'accesso vtable, vedere Associazione tardiva e accesso Vtable nel modello di estensione [ADSI.](late-binding-vs--vtable-access-in-the-adsi-extension-model.md)

Poiché tutti gli oggetti estensione reindirizzano [**le funzioni IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) all'aggregatore, l'aggregatore controlla quale **Func1** viene richiamato. Le regole sono:

-   Se una qualsiasi interfaccia e ne sarà presente una sola, se presente, nell'aggregatore (ADSI) supporta una funzione denominata **Func1**, l'aggregatore richiama il proprio **Func1**.
-   In caso contrario, l'aggregatore passa attraverso ognuna delle relative estensioni, nell'ordine elencato nel Registro di sistema, e trova la prima estensione che implementa una funzione denominata **Func1**. È possibile, ma improbabile, che più interfacce [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) duali in questa prima estensione abbia una funzione denominata **Func1**. L'estensione deve determinare **quale Func1** deve sempre essere richiamato in Automazione.

## <a name="same-function-name-with-different-parameters"></a>Stesso nome di funzione con parametri diversi

Nella sezione precedente è stato illustrato come risolvere i conflitti di nomi di funzione, vale a esempio i nomi di funzione con lo stesso nome di funzione e lo stesso elenco di parametri, ad esempio numero, tipo e ordine, quando si verifica in Automazione. Cosa succede se due funzioni hanno lo stesso nome ma parametri diversi? Se un client ADSI richiama la funzione usando [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) senza usare più nomi per specificare i parametri, il modello di estensione ADSI non può disambiguare le funzioni. In base all'schema di risoluzione descritto in precedenza, la prima estensione del Registro di sistema che supporta questa funzione tramite una delle relative interfacce ha la versione di questa funzione richiamata e la chiamata potrebbe non riuscire o produrre risultati non corretti.

Esempio:

-   Extn1 (primo nel Registro di sistema nella classe CA - priorità più alta) supporta **IInterface1**.
-   Extn2 (terzo nel Registro di sistema nella classe CA - priorità inferiore) supporta **IInterface2**.
-   **IInterface1** supporta **Method1(int param1, int param2)**.
-   **IInterface2** supporta **Method1(int param1)**.

Un client ADSI ha un puntatore a [**interfaccia IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) a un oggetto della classe CA. Vuole richiamare **IInterface2::Method1**. Se il client chiama "pDispatch->GetIDsOfNames(IID \_ NULL, rgszNames, 1, MY LCID, rgDispId)" archiviando semplicemente il nome della funzione \_ "Method1" in *rgszNames \[ 0, \]* viene richiamato **IInterface1::Method1** anziché **L'interfaccia IInterface2::Method1** desiderata e la funzione ha esito negativo perché il numero di parametri è diverso.

Per ridurre al minimo questo problema, gli sviluppatori di estensioni possono antesciare i nomi delle funzioni con i propri identificatori specifici ed evitare progettazioni di interfacce che usano funzioni con lo stesso nome, ma parametri diversi.

Se si verifica un conflitto di nomi, i client ADSI possono evitare il problema tramite l'accesso vtable diretto se l'interfaccia è un'interfaccia duale. Se l'accesso vtable diretto non è possibile, i client ADSI devono chiamare [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) con più nomi, specificando i nomi delle funzioni e i parametri nella matrice *rgszNames* descritta in precedenza.

Visual Basic 5 non chiama la [**funzione IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) con più nomi. Ciò significa che passa solo il nome della funzione **a GetIDsOfNames,** ma non agli argomenti. Tuttavia, Visual Basic 5 consente agli utenti di richiamare una funzione tramite l'accesso vtable diretto, anziché chiamare la funzione **IDispatch::GetIDsOfNames** se l'interfaccia è un'interfaccia duale. Gli sviluppatori devono usare l'accesso vtable diretto, se possibile.

Per altre informazioni sulla risoluzione dei conflitti di nomi, vedere [Esempio per la risoluzione dei conflitti dei nomi di funzione](example-for-resolving-function-name-conflicts.md).

 

 