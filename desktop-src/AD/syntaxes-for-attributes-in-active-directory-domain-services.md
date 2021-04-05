---
title: Sintassi per gli attributi in Active Directory Domain Services
description: Active Directory Domain Services definire un set di sintassi degli attributi per specificare il tipo di dati contenuti in un attributo.
ms.assetid: 79d27d47-5d03-4ad6-bf97-c387c34fa454
ms.tgt_platform: multiple
keywords:
- Sintassi per gli attributi di Active Directory Domain Services Active Directory
- Attributi Active Directory, sintassi per
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04386e1b4981a81585fe208afa4cca6ed02d4c3c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104117523"
---
# <a name="syntaxes-for-attributes-in-active-directory-domain-services"></a>Sintassi per gli attributi in Active Directory Domain Services

Active Directory Domain Services definire un set di sintassi degli attributi per specificare il tipo di dati contenuti in un attributo. Le sintassi predefinite non vengono effettivamente visualizzate nella directory e non è possibile aggiungere nuove sintassi. Per identificare la sintassi di una classe Attribute è possibile utilizzare diversi metodi:

-   I metodi [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get), [**IADs. GetEx**](/windows/desktop/api/iads/nf-iads-iads-getex), [**IADs. Put**](/windows/desktop/api/iads/nf-iads-iads-put)e [**IADs. PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) usano la struttura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) per ottenere e impostare i valori degli attributi di un oggetto. Il membro **VT** di questa struttura è un valore **VarType** che identifica il tipo di dati.
-   I metodi delle interfacce [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) e [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) utilizzano un valore dell'enumerazione [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) per specificare il tipo di dati.
-   Per specificare la sintassi di una nuova classe Attribute, impostare gli attributi [**attributeSyntax**](/windows/desktop/ADSchema/a-attributesyntax) e [**oMSyntax**](/windows/desktop/ADSchema/a-omsyntax) di un oggetto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) . Se il valore di **oMSyntax** è 127, è necessario impostare anche l'attributo [**oMObjectClass**](/windows/desktop/ADSchema/a-omobjectclass) . Per ulteriori informazioni, vedere [scelta di una sintassi](choosing-a-syntax.md).

Per un elenco completo delle sintassi fornite da Active Directory Domain Services, inclusi i valori **VarType** e [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) corrispondenti di ogni sintassi, vedere [sintassi](/windows/desktop/ADSchema/syntaxes).

 

 