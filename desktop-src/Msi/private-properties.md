---
description: Le proprietà private vengono usate internamente dal programma di installazione e i relativi valori devono essere immessi nel database dall'autore del pacchetto di installazione o impostati dal programma di installazione durante l'installazione su valori determinati dall'ambiente operativo.
ms.assetid: 7d574bf0-bcb3-4e19-9659-fe741ace9f21
title: Proprietà private
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d166f876bb953008a6920c3089fab5974ebbb05909c1b41db299212ee069dd8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558417"
---
# <a name="private-properties"></a>Proprietà private

Le proprietà private vengono usate internamente dal programma di installazione e i relativi valori devono essere immessi nel database dall'autore del pacchetto di installazione o impostati dal programma di installazione durante l'installazione su valori determinati dall'ambiente operativo. L'unico modo in cui un utente può interagire con le proprietà private è tramite Eventi [di controllo](control-events.md) nell'interfaccia utente del pacchetto creato. I nomi delle proprietà private devono includere lettere minuscole. Vedere [Restrizioni relative ai nomi delle proprietà.](restrictions-on-property-names.md)

Le proprietà private descrivono in genere l'ambiente operativo. Ad esempio, se l'installazione viene eseguita in una piattaforma Windows, il programma di installazione imposta la proprietà [**WindowsFolder**](windowsfolder.md) sul valore specificato nella tabella Property.

Non è possibile eseguire l'override dei valori delle proprietà private in una riga di comando. Per cancellare una proprietà privata da un'installazione, lasciarla fuori dalla [tabella Proprietà](property-table.md). In Windows XP e Windows 2000 non è possibile impostare una proprietà privata nella fase dell'interfaccia utente dell'installazione e quindi passare il valore alla fase di esecuzione.

Per un elenco di tutte le proprietà private standard usate dal programma di installazione, vedere [Riferimento alle proprietà.](property-reference.md) È possibile definire una proprietà privata personalizzata immettendo il nome e il valore iniziale della proprietà nella tabella Proprietà. I nomi delle proprietà private devono sempre includere lettere minuscole.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà pubbliche](public-properties.md)
</dt> </dl>

 

 



