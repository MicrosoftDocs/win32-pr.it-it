---
title: Ereditarietà della classe nello schema Active Directory
description: Tutte le classi di oggetti in uno schema del servizio di Active Directory directory sono derivate dalla classe speciale top.
ms.assetid: 26e5107f-8204-4f64-bd07-b5b4f16103f4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd550a3eed6aeb633f6db265260b6c65c17f993
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046550"
---
# <a name="class-inheritance-in-the-active-directory-schema"></a>Ereditarietà della classe nello schema Active Directory

Tutte le classi di oggetti in uno schema del servizio di Active Directory directory sono derivate dalla classe speciale [**Top**](/windows/desktop/ADSchema/c-top). Ad eccezione di **Top**, tutte le classi di oggetti sono sottoclassi di un'altra classe di oggetti. Ad esempio, [**Contact**](/windows/desktop/ADSchema/c-contact) è una sottoclasse di [**OrganizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson); **OrganizationalPerson** è una sottoclasse di [**Person**](/windows/desktop/ADSchema/c-person); e **Person** è una sottoclasse di **Top**. L'attributo [**subclassOf**](/windows/desktop/ADSchema/a-subclassof) di un oggetto [**classSchema**](/windows/desktop/ADSchema/c-classschema) è una proprietà a valore singolo che indica la superclasse immediata della classe.

Alcuni dei valori di attributo che definiscono una classe vengono ereditati dalle relative superclassi. Quindi, la classe [**Contact**](/windows/desktop/ADSchema/c-contact) eredita i valori dalle relative superclassi, ovvero le classi [**OrganizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson), [**Person**](/windows/desktop/ADSchema/c-person)e [**Top**](/windows/desktop/ADSchema/c-top) . Una classe eredita i dati seguenti dalle relative superclassi:

-   Attributi possibili: i valori degli attributi [**mustContain**](/windows/desktop/ADSchema/a-mustcontain), [**mayContain**](/windows/desktop/ADSchema/a-maycontain), [**systemMustContain**](/windows/desktop/ADSchema/a-systemmustcontain)e [**systemMayContain**](/windows/desktop/ADSchema/a-systemmaycontain) di un oggetto [**classSchema**](/windows/desktop/ADSchema/c-classschema) definiscono un elenco completo degli attributi che è possibile impostare in un'istanza della classe di oggetti. Per ogni classe di oggetti, i valori di questi attributi includono tutti i valori ereditati dalle relative superclassi, nonché tutti i valori impostati in modo esplicito per la classe di oggetti. Pertanto, l'attributo [**mustContain**](/windows/desktop/ADSchema/a-mustcontain) della classe [**OrganizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson) include tutti i valori **mustContain** ereditati dalle classi [**Person**](/windows/desktop/ADSchema/c-person) e [**Top**](/windows/desktop/ADSchema/c-top) , nonché da eventuali valori **mustContain** impostati in modo esplicito nella classe **OrganizationalPerson** .
-   Possibili elementi padre nella gerarchia di directory: i valori degli attributi [**possSuperiors**](/windows/desktop/ADSchema/a-posssuperiors) e [**systemPossSuperiors**](/windows/desktop/ADSchema/a-systemposssuperiors) di un oggetto [**classSchema**](/windows/desktop/ADSchema/c-classschema) definiscono un elenco completo delle classi di oggetti che possono contenere un'istanza della classe di oggetti. Per ogni classe di oggetti, i valori includono quelli ereditati dalle relative superclassi, nonché quelli impostati in modo esplicito per la classe di oggetti.

Tenere presente che la classe di oggetti può avere anche molte classi ausiliarie, specificate negli attributi [**auxiliaryClass**](/windows/desktop/ADSchema/a-auxiliaryclass) e [**systemAuxiliaryClass**](/windows/desktop/ADSchema/a-systemauxiliaryclass) di un oggetto **classSchema** . Una classe di oggetti eredita i valori [**mustContain**](/windows/desktop/ADSchema/a-mustcontain), [**mayContain**](/windows/desktop/ADSchema/a-maycontain), [**systemMustContain**](/windows/desktop/ADSchema/a-systemmustcontain)e [**systemMayContain**](/windows/desktop/ADSchema/a-systemmaycontain) dalle classi ausiliarie.

 

 