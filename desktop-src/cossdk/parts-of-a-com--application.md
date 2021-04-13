---
description: Le applicazioni COM+ sono costituite da uno o più componenti COM.
ms.assetid: e7ed2844-276e-4726-952d-e4d3be2eb6e8
title: Parti di un'applicazione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f75aba454689e25e8706d4a7e3f059d498891f9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483029"
---
# <a name="parts-of-a-com-application"></a>Parti di un'applicazione COM+

Le applicazioni COM+ sono costituite da uno o più componenti COM.

In tutta la documentazione COM+ vengono utilizzati i termini seguenti:

<dl> <dt>

<span id="COM_component"></span><span id="com_component"></span><span id="COM_COMPONENT"></span>*Componente COM*
</dt> <dd>

Unità binaria di codice che crea oggetti COM (include il codice per la creazione di pacchetti e la registrazione).

</dd> <dt>

<span id="COM_object"></span><span id="com_object"></span><span id="COM_OBJECT"></span>*Oggetto COM*
</dt> <dd>

Istanza di una classe COM.

</dd> <dt>

<span id="COM_class"></span><span id="com_class"></span><span id="COM_CLASS"></span>*Classe COM*
</dt> <dd>

Implementazione concreta denominata di una o più interfacce. Una classe COM è identificata da un CLSID (talvolta anche da un ProgID).

</dd> <dt>

<span id="COM_interface"></span><span id="com_interface"></span><span id="COM_INTERFACE"></span>*Interfaccia COM*
</dt> <dd>

Gruppo di funzioni di metodo correlate esposte da una classe COM che specifica un contratto. Sono inclusi il nome, la firma dell'interfaccia, la semantica dell'interfaccia e il formato del buffer di marshalling. Un'interfaccia viene identificata da un IID. La sintassi dell'interfaccia è definita nelle librerie di tipi e/o IDL. Le interfacce di una classe COM devono essere divise in set di metodi gestibili e coesi.

Le interfacce COM non sono modificabili. il contratto COM indica che non è possibile modificarli. Qualsiasi modifica, ad esempio l'aggiunta di metodi, richiede la definizione di una nuova interfaccia.

</dd> <dt>

<span id="COM_method"></span><span id="com_method"></span><span id="COM_METHOD"></span>*Metodo COM*
</dt> <dd>

Uno di un set di funzioni correlate fornite da un'interfaccia COM.

</dd> </dl>

## <a name="configured-and-unconfigured-components"></a>Componenti configurati e non configurati

Per sfruttare i servizi supportati dalle applicazioni COM+, l'ambiente COM+ impone requisiti specifici sui componenti COM compilati per le applicazioni COM+. Quando viene aggiunto a un'applicazione COM+, un componente COM è noto come *componente configurato*.

I componenti COM compilati per le applicazioni COM+ sono componenti server in-process. Il componente deve contenere una libreria dei tipi (file tlb) per descrivere tutte le classi implementate nel componente e dichiarare le interfacce per tutte le classi nel componente. È possibile creare e implementare questi componenti con Microsoft Visual Basic, Microsoft Visual C++ o qualsiasi strumento di sviluppo compatibile con COM.

Un *componente non configurato* è un componente che non viene installato in un'applicazione com+. È possibile trasformare la maggior parte dei componenti non configurati in componenti configurati semplicemente mediante l'integrazione in un'applicazione COM+.

> [!Note]  
> Non utilizzare lo stesso AppID per un'applicazione COM+ e nel registro di sistema per un componente non configurato. Quando il componente non configurato viene attivato, l'attivazione può recuperare le informazioni dell'applicazione COM+ dal registro di sistema che non contiene le informazioni necessarie per l'attivazione COM. Potrebbero verificarsi problemi simili se viene effettuata una chiamata a [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) da Dllhost che ospita l'applicazione server com+.

 

 

 
