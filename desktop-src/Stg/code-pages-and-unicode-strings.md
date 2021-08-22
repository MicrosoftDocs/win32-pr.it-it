---
title: Code Pages e stringhe Unicode
description: Un'altra considerazione da tenere in considerazione nell'implementazione di IPropertySetStorage è il modo in cui i nomi delle proprietà Unicode vengono archiviati nell'ID proprietà 0 (dizionario dei nomi delle proprietà), che non usa stringhe Unicode.
ms.assetid: 830c90c9-d2a5-4ecf-8cb6-9950ed5320bf
keywords:
- Code Pages e stringhe Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a1d5a830d3d4e2fccbb61563e7a8a0447d74e7c427e5e2e0434e7194a2ad3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663601"
---
# <a name="code-pages-and-unicode-strings"></a>Code Pages e stringhe Unicode

Un'altra considerazione da tenere in considerazione nell'implementazione di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) è il modo in cui i nomi delle proprietà Unicode vengono archiviati nell'ID proprietà 0 (dizionario dei nomi delle proprietà), che non usa stringhe Unicode.

Unicode ha ufficialmente un valore di tabella codici pari a 1200. Per archiviare i valori Unicode nel dizionario dei nomi delle proprietà, usare un valore della tabella codici 1200 per l'intero set di proprietà (nell'ID proprietà 1), specificato dall'assenza del flag **\_ ANSI PROPSETFLAG** in [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create). Tenere presente che ciò ha l'effetto collaterale di archiviare tutti i valori stringa nel set di proprietà in Unicode. In tutte le pagine di codice, il conteggio trovato all'inizio di un **\_ LPSTR VT** è un numero di byte, non un numero di caratteri. Questa operazione è necessaria per garantire la compatibilità con i client di versioni precedenti.

L'implementazione di file composti [**di IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) crea tutti i nuovi set di proprietà completamente in Unicode (tabella codici 1200) o nella tabella codici ANSI del sistema corrente. Ciò è controllato dall'assenza o dalla presenza del flag **\_ ANSI PROPSETFLAG** nel parametro *grfFlags* di [**IPropertySetStorage::Create.**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)

Creare e aprire set di proprietà come Unicode. Per implementare questa funzionalità, non impostare il flag **\_ ANSI PROPSETFLAG** nel parametro *grfFlags* di [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create). Evitare di **usare valori \_ LPSTR VT** e usare invece **valori \_ LPWSTR VT.** Quando la tabella codici del set di proprietà è Unicode, i valori di stringa **\_ LPSTR VT** vengono convertiti in Unicode quando vengono archiviati e di nuovo in valori stringa multibyte quando vengono recuperati.

L'impostazione del flag **\_ ANSI PROPSETFLAG** come segnalato tramite una chiamata a [**IPropertyStorage::Stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat) indica se la tabella codici sottostante è o meno Unicode. Tenere presente che l'ID proprietà 1 può essere letto in modo esplicito per apprendere la tabella codici.

È possibile accedere all'ID proprietà 1 tramite una chiamata a [**IPropertyStorage::ReadMultiple.**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) Tuttavia, è di sola lettura e potrebbe non essere aggiornato con [**WriteMultiple.**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) Inoltre, potrebbe non essere eliminato con [**DeleteMultiple.**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)

 

 




