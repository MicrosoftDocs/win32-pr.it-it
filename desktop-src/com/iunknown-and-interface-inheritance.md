---
title: IUnknown ed ereditarietà dell'interfaccia
description: IUnknown ed ereditarietà dell'interfaccia
ms.assetid: c45f0947-6020-4aa1-9250-561603a46a68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce4d9d164607745b78001bb92b7dc5331296abe
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300534"
---
# <a name="iunknown-and-interface-inheritance"></a>IUnknown ed ereditarietà dell'interfaccia

L'ereditarietà in COM non implica il riutilizzo del codice. Poiché non vi sono implementazioni associate a interfacce, l'ereditarietà dell'interfaccia non implica l'ereditarietà del codice. Significa solo che il contratto associato a un'interfaccia viene ereditato in una classe di base virtuale pura C++ e modificato, aggiungendo nuovi metodi o qualificando ulteriormente l'utilizzo consentito dei metodi. In COM non esiste alcuna ereditarietà selettiva. Se un'interfaccia eredita da un'altra, include tutti i metodi definiti dall'altra interfaccia.

L'ereditarietà viene utilizzata sporadicamente nelle interfacce COM predefinite. Tutte le interfacce predefinite (e tutte le interfacce personalizzate definite) ereditano le definizioni dall'interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)importante, che contiene tre metodi fondamentali: [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Tutti gli oggetti COM devono implementare l'interfaccia **IUnknown** perché fornisce i mezzi, usando **QueryInterface**, per spostarsi liberamente tra le diverse interfacce supportate da un oggetto e i mezzi per gestirne la durata usando **AddRef** e **Release**.

Quando si crea un oggetto che supporta l' [aggregazione](aggregation.md), è necessario implementare un set di funzioni [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) per tutte le interfacce e un'interfaccia **IUnknown** autonoma. In ogni caso, qualsiasi implementatore di oggetti implementerà i metodi **IUnknown** . Per ulteriori informazioni, vedere la sezione [utilizzo e implementazione di IUnknown](using-and-implementing-iunknown.md) .

Sebbene esistano alcune interfacce che ereditano le definizioni da una seconda interfaccia oltre a [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), la maggior parte eredita semplicemente i metodi di interfaccia **IUnknown** . In questo modo, la maggior parte delle interfacce risulta relativamente compatta e facile da incapsulare.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti e interfacce COM](com-objects-and-interfaces.md)
</dt> </dl>

 

 