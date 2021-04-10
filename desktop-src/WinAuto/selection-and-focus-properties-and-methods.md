---
title: Proprietà e metodi di selezione e messa a fuoco
description: Analogamente a molti elementi in applicazioni in esecuzione su sistemi operativi Microsoft Windows, gli oggetti accessibili selezionano e ricevono lo stato attivo. Questi attributi consentono agli utenti di interagire con gli elementi dell'applicazione, modificare i valori e manipolarli in altro modo.
ms.assetid: 8170fe19-f157-4d7d-8eec-d384e51f1560
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bbb5eee361707ec4876245eef5b0eb352f8dfd6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728431"
---
# <a name="selection-and-focus-properties-and-methods"></a>Proprietà e metodi di selezione e messa a fuoco

Analogamente a molti elementi in applicazioni in esecuzione su sistemi operativi Microsoft Windows, gli oggetti accessibili *selezionano* e ricevono lo *stato attivo*. Questi attributi consentono agli utenti di interagire con gli elementi dell'applicazione, modificare i valori e manipolarli in altro modo.

Esistono alcune differenze principali tra la selezione degli oggetti e lo stato attivo dell'oggetto:

-   Un oggetto con stato attivo è l'unico oggetto nell'intero sistema operativo che riceve l'input da tastiera. L'oggetto con lo stato attivo della tastiera è la finestra attiva o un oggetto figlio della finestra attiva.
-   Un oggetto selezionato è contrassegnato per partecipare a un determinato tipo di operazione di gruppo.

Ad esempio, un utente può selezionare più elementi in un controllo visualizzazione elenco, ma lo stato attivo viene assegnato solo a un oggetto nel sistema alla volta. Si noti che gli elementi con stato attivo sono da una selezione di elementi.

I client determinano se un particolare oggetto accessibile o elemento figlio ha lo stato attivo chiamando [**IAccessible:: Get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus). I client determinano se un oggetto è selezionato o quali elementi figlio all'interno di un oggetto accessibile sono selezionati chiamando [**IAccessible:: Get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection). Per oggetti quali i controlli di visualizzazione elenco in cui sono selezionati più elementi figlio, l'oggetto padre deve supportare l'interfaccia [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) , che consente ai client di enumerare gli elementi figlio selezionati.

## <a name="events-triggered-in-menus"></a>Eventi attivati nei menu

Microsoft Active Accessibility espone i menu standard creati con le API dei menu e i file di risorse di Microsoft Win32. Per coerenza con i menu standard, i server con menu personalizzati attivano lo [**\_ \_ stato attivo dell'oggetto evento**](event-constants.md), non la [**\_ \_ selezione di oggetti evento**](event-constants.md), quando un utente evidenzia una voce di menu.

> [!Note]  
> Microsoft Active Accessibility non supporta la selezione del testo contenuto nei controlli Edit e Rich Edit perché il testo viene esposto come una singola stringa nella proprietà [**value**](value-property.md) di questi controlli.

 

## <a name="in-this-section"></a>Contenuto della sezione

-   [Selezione di oggetti figlio](selecting-child-objects.md)

 

 