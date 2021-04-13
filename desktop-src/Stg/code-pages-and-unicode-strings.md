---
title: Tabelle codici e stringhe Unicode
description: Un'altra considerazione nell'implementazione di IPropertySetStorage è il modo in cui i nomi delle proprietà Unicode vengono archiviati nell'ID di proprietà 0 (il dizionario del nome della proprietà), che non utilizza stringhe Unicode.
ms.assetid: 830c90c9-d2a5-4ecf-8cb6-9950ed5320bf
keywords:
- Tabelle codici e stringhe Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 508d508ec21e7e763a683e534cf485ebbeec018d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328719"
---
# <a name="code-pages-and-unicode-strings"></a>Tabelle codici e stringhe Unicode

Un'altra considerazione nell'implementazione di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) è il modo in cui i nomi delle proprietà Unicode vengono archiviati nell'ID di proprietà 0 (il dizionario del nome della proprietà), che non utilizza stringhe Unicode.

Unicode ha ufficialmente un valore della tabella codici 1200. Per archiviare i valori Unicode nel dizionario nome proprietà, usare un valore della tabella codici 1200 per l'intero set di proprietà (in ID proprietà 1), specificato dall'assenza del flag **\_ ANSI PROPSETFLAG** in [**IPropertySetStorage:: create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create). Tenere presente che questa operazione ha effetto collaterale sull'archiviazione di tutti i valori stringa nella proprietà impostata in Unicode. In tutte le tabelle codici il conteggio rilevato all'inizio di un **\_ LPSTR VT** è un conteggio di byte, non un conteggio di caratteri. Questa operazione è necessaria per garantire la compatibilità con i client di versioni precedenti.

L'implementazione del file composto di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) crea completamente tutti i nuovi set di proprietà in formato Unicode (tabella codici 1200) o nella tabella codici ANSI di sistema corrente. Questa operazione è controllata dall'assenza o dalla presenza del **flag \_ ANSI PROPSETFLAG** nel parametro *grfFlags* di [**IPropertySetStorage:: create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create).

Creare e aprire i set di proprietà come Unicode. Per implementare questo, non impostare il flag **\_ ANSI PROPSETFLAG** nel parametro *grfFlags* di [**IPropertySetStorage:: create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create). Evitare di usare i valori **\_ LPSTR di VT** e usare invece i valori **\_ LPWSTR di VT** . Quando la tabella codici della proprietà è impostata su Unicode, i valori di stringa **VT \_ LPSTR** vengono convertiti in Unicode quando vengono archiviati e restituiti a valori stringa multibyte quando vengono recuperati.

L'impostazione del flag **\_ ANSI PROPSETFLAG** come segnalato tramite una chiamata a [**IPropertyStorage:: stat indica**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat) se la tabella codici sottostante è o non è Unicode. Tenere presente che l'ID di proprietà 1 può essere letto in modo esplicito per apprendere la tabella codici.

È possibile accedere all'ID di proprietà 1 tramite una chiamata a [**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple). Tuttavia, è di sola lettura e non può essere aggiornato con [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple). Inoltre, non può essere eliminato con [**DeleteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple).

 

 




