---
description: Un provider di proprietà utilizza i metodi IWbemPropertyProvider come interfaccia principale di WMI. Con IWbemPropertyProvider è possibile implementare il codice per recuperare e modificare le proprietà di classe e istanza.
ms.assetid: d08c2ca4-9f8a-4a27-80fc-688d7c56f5eb
ms.tgt_platform: multiple
title: Implementazione dell'interfaccia primaria per un provider di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 942117547380000e0da7d22a5e933cba4b3ffced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315213"
---
# <a name="implementing-the-primary-interface-for-a-property-provider"></a>Implementazione dell'interfaccia primaria per un provider di proprietà

Un provider di proprietà utilizza i metodi [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) come interfaccia principale di WMI. Con **IWbemPropertyProvider** è possibile implementare il codice per recuperare e modificare le proprietà di classe e istanza.

Nella tabella seguente sono elencati i metodi [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) che è possibile implementare per un provider di proprietà.



| Metodo                                                   | Funzionalità      |
|----------------------------------------------------------|--------------|
| [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) | Recupero    |
| [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) | Modifica |



 

> [!Note]  
> È necessario implementare un provider di proprietà come provider in-process. WMI inizializza i provider di proprietà scritti come servizi o file eseguibili, ma non chiama mai i metodi [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) e [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) .

 

Se si sceglie di non supportare uno di questi metodi, il provider può fornire un'implementazione stub che restituisce **il \_ provider WBEM E \_ \_ non \_ idoneo**.

Un provider di proprietà identifica una classe o un'istanza gestita da un set di tre qualificatori: **PropertyContext**, **InstanceContext** e **ClassContext**. WMI passerà le costanti stringa che descrivono questi tre qualificatori al provider di proprietà.

Il provider di proprietà deve essere preparato a gestire i seguenti tipi di qualificatori di contesto:

-   Il qualificatore **InstanceContext** è associato a un'istanza e contiene informazioni che si applicano a ogni proprietà nell'istanza.
-   Il qualificatore **ClassContext** è associato a una classe e contiene informazioni che si applicano a ogni istanza della classe. Ad esempio, in una classe utilizzata per archiviare i dati forniti dal provider del registro di sistema, **ClassContext** può essere il percorso della chiave del registro di sistema che contiene le proprietà da segnalare.
-   Il qualificatore **PropertyContext** specifica informazioni specifiche del contesto relative alla proprietà. Ad esempio, in una classe utilizzata per archiviare i dati forniti dal provider del registro di sistema, **PropertyContext** specifica il nome del valore del registro di sistema da archiviare con la proprietà.

Questi qualificatori possono interagire tra loro. È possibile designare sia un valore **InstanceContext** che **PropertyContext** per indicare al provider come trattare particolari tipi di istanze. È possibile, ad esempio, contrassegnare le istanze che il provider rileverà come leggibile, ma che disponga di una sola proprietà scrivibile.

Il qualificatore più comune usato è **PropertyContext**. Pertanto, WMI fornisce il qualificatore **DynProps** come collegamento. WMI considera ogni proprietà di un'istanza contrassegnata con **DynProps** per avere anche i qualificatori **Dynamic**, [**provider**](/windows/desktop/api/Provider/nl-provider-provider)e **PropertyContext** .

 

 



