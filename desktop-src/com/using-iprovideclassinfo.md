---
title: Uso di IProvideClassInfo
description: Uso di IProvideClassInfo
ms.assetid: 16541aab-474f-4ae5-a6b6-fb2fea6d38ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32a3abd61bb330a2a7d681b6d53648c5fbde8c53
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047433"
---
# <a name="using-iprovideclassinfo"></a>Uso di IProvideClassInfo

Un oggetto collegabile può offrire le interfacce [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) e [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) in modo che i client possano facilmente esaminare le informazioni sul tipo. Questa funzionalità è importante quando si gestiscono le interfacce in uscita, che, per definizione, sono definite da un oggetto ma implementate da un client sul relativo oggetto sink. In alcuni casi, un'interfaccia in uscita è nota in fase di compilazione sia per l'oggetto collegabile che per l'oggetto sink; Questo è il caso di [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink).

In altri casi, tuttavia, solo l'oggetto collegabile conosce le definizioni di interfaccia in uscita in fase di compilazione. In questi casi, il client deve ottenere le informazioni sul tipo per l'interfaccia in uscita, in modo che sia in grado di fornire dinamicamente un sink che supporta i punti di ingresso corretti, come indicato di seguito:

1.  Il client enumera i punti di connessione e quindi, per ottenere l'IID delle interfacce in uscita supportate dall'oggetto collegabile, chiama [**IConnectionPoint:: GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) per ogni punto di connessione.
2.  Il client esegue una query sull'oggetto collegabile per una delle interfacce [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) .
3.  Il client chiama i metodi nelle interfacce [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) per ottenere le informazioni sul tipo per l'interfaccia in uscita.
4.  Il client crea un oggetto sink che supporta l'interfaccia in uscita.
5.  Il processo continua e il client chiama [**IConnectionPoint:: Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) per connettere il sink al punto di connessione.

Nelle informazioni sul tipo, l' [**origine**](/windows/desktop/Midl/source) dell'attributo contrassegna un' [**interfaccia**](/windows/desktop/Midl/interface) o un'interfaccia [**Dispatch**](/windows/desktop/Midl/dispinterface) elencata sotto una [**coclasse**](/windows/desktop/Midl/coclass) come interfaccia in uscita. Quelli elencati senza questo attributo sono considerati interfacce in ingresso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce di oggetti collegabili](connectable-object-interfaces.md)
</dt> <dt>

[Fornire informazioni sulla classe](providing-class-information.md)
</dt> </dl>

 

 