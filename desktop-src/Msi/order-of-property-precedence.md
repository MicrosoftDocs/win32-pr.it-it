---
description: Il programma di installazione imposta le proprietà utilizzando il seguente ordine di precedenza. Un valore di proprietà in questo elenco può eseguire l'override di un valore che viene seguito e sottoposto a override da un valore che lo precede nell'elenco.
ms.assetid: ba9240fe-2e5a-43f5-8cdf-59dd6348092b
title: Ordine di precedenza delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90c114594b9a825a3847db37f5b98dc990211d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319000"
---
# <a name="order-of-property-precedence"></a>Ordine di precedenza delle proprietà

Il programma di installazione imposta le proprietà utilizzando il seguente ordine di precedenza. Un valore di proprietà in questo elenco può eseguire l'override di un valore che viene seguito e sottoposto a override da un valore che lo precede nell'elenco.

1.  Proprietà specificate dall'ambiente operativo.
2.  [Proprietà pubbliche](public-properties.md) impostate nella riga di comando.
3.  Proprietà pubbliche elencate da [**AdminProperties**](adminproperties.md) PropertySet durante un' [installazione amministrativa](administrative-installation.md) .
4.  Proprietà pubbliche o private impostate durante l'applicazione di una [*trasformazione*](t-gly.md).
5.  Proprietà pubblica o privata impostata mediante la creazione della [tabella delle proprietà](property-table.md) del file con estensione msi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulle proprietà](about-properties.md)
</dt> </dl>

 

 



