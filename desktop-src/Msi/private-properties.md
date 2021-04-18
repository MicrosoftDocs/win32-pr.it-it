---
description: Le proprietà private vengono utilizzate internamente dal programma di installazione e i rispettivi valori devono essere immessi nel database dall'autore del pacchetto di installazione o impostati dal programma di installazione durante l'installazione ai valori determinati dall'ambiente operativo.
ms.assetid: 7d574bf0-bcb3-4e19-9659-fe741ace9f21
title: Proprietà private
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab7b0196be016fecb625e139f308219582620d40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315468"
---
# <a name="private-properties"></a>Proprietà private

Le proprietà private vengono utilizzate internamente dal programma di installazione e i rispettivi valori devono essere immessi nel database dall'autore del pacchetto di installazione o impostati dal programma di installazione durante l'installazione ai valori determinati dall'ambiente operativo. L'unico modo in cui un utente può interagire con le proprietà private è tramite [gli eventi di controllo](control-events.md) nell'interfaccia utente creata del pacchetto. I nomi delle proprietà private devono includere lettere minuscole. Vedere [restrizioni sui nomi di proprietà](restrictions-on-property-names.md).

Le proprietà private in genere descrivono l'ambiente operativo. Se, ad esempio, l'installazione viene eseguita in una piattaforma Windows, il programma di installazione imposta la proprietà [**WindowsFolder**](windowsfolder.md) sul valore specificato nella tabella delle proprietà.

Non è possibile eseguire l'override dei valori delle proprietà private in una riga di comando. Per cancellare una proprietà privata da un'installazione, lasciarla fuori dalla [tabella delle proprietà](property-table.md). In Windows XP e Windows 2000 non è possibile impostare una proprietà privata nella fase dell'interfaccia utente dell'installazione, quindi passare il valore alla fase di esecuzione.

Per un elenco di tutte le proprietà private standard usate dal programma di installazione, vedere [riferimento alle proprietà](property-reference.md). È possibile definire una proprietà privata personalizzata immettendo il nome e il valore iniziale della proprietà nella tabella delle proprietà. I nomi delle proprietà private devono sempre includere lettere minuscole.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà pubbliche](public-properties.md)
</dt> </dl>

 

 



