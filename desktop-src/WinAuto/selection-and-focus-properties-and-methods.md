---
title: Metodi e proprietà di selezione e stato attivo
description: Come molti elementi nelle applicazioni in esecuzione nei sistemi operativi Microsoft Windows, gli oggetti accessibili selezionano e ricevono lo stato attivo della tastiera. Questi attributi consentono agli utenti di interagire con gli elementi dell'applicazione, modificare i valori e modificarli in altro modo.
ms.assetid: 8170fe19-f157-4d7d-8eec-d384e51f1560
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bf5c5bc4a60e664c124e7181f998d9e0a7af6ab82ef9b2d4f030f7541d530ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745230"
---
# <a name="selection-and-focus-properties-and-methods"></a>Metodi e proprietà di selezione e stato attivo

Come molti elementi nelle applicazioni in esecuzione nei sistemi operativi Microsoft Windows, gli oggetti accessibili *selezionano* e ricevono lo stato attivo della *tastiera.* Questi attributi consentono agli utenti di interagire con gli elementi dell'applicazione, modificare i valori e modificarli in altro modo.

Esistono alcune differenze principali tra la selezione di oggetti e lo stato attivo dell'oggetto:

-   Un oggetto con stato attivo è l'unico oggetto dell'intero sistema operativo che riceve l'input da tastiera. L'oggetto con lo stato attivo della tastiera è la finestra attiva o un oggetto figlio della finestra attiva.
-   Un oggetto selezionato è contrassegnato per partecipare a un tipo di operazione di gruppo.

Ad esempio, un utente può selezionare più elementi in un controllo visualizzazione elenco, ma lo stato attivo viene assegnato solo a un oggetto del sistema alla volta. Si noti che gli elementi con stato attivo derivano da una selezione di elementi.

I client determinano se un particolare oggetto accessibile o elemento figlio ha lo stato attivo chiamando [**IAccessible::get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus). I client determinano se un oggetto è selezionato o quali elementi figlio all'interno di un oggetto accessibile vengono selezionati chiamando [**IAccessible::get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection). Per oggetti come i controlli visualizzazione elenco in cui sono selezionati più elementi figlio, l'oggetto padre deve supportare [l'interfaccia IEnumVARIANT,](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) che consente ai client di enumerare gli elementi figlio selezionati.

## <a name="events-triggered-in-menus"></a>Eventi attivati nei menu

Microsoft Active Accessibility i menu standard creati con le API del menu Microsoft Win32 e i file di risorse. Per coerenza con i menu standard, i server con menu personalizzati attivano [**EVENT \_ OBJECT \_ FOCUS**](event-constants.md)e non [**EVENT OBJECT \_ \_ SELECTION**](event-constants.md)quando un utente evidenzia una voce di menu.

> [!Note]  
> Microsoft Active Accessibility non supporta la selezione del testo contenuto nei controlli di modifica e rich edit perché il testo viene esposto come singola stringa nella proprietà [**Value**](value-property.md) per questi controlli.

 

## <a name="in-this-section"></a>Contenuto della sezione

-   [Selezione di oggetti figlio](selecting-child-objects.md)

 

 