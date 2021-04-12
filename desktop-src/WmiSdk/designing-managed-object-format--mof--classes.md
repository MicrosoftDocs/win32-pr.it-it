---
description: Un provider WMI è costituito da un file Managed Object Format (MOF) e da un file DLL. Il file MOF definisce le classi per le quali l'implementazione del provider fornisce i dati.
ms.assetid: 20ef6b88-2aaa-4e86-bc4a-bebc34069672
ms.tgt_platform: multiple
title: Progettazione di classi Managed Object Format (MOF)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 201f8c45f7a247fbca5695baa6dd440fc5dc323f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232405"
---
# <a name="designing-managed-object-format-mof-classes"></a>Progettazione di classi Managed Object Format (MOF)

Un [*provider WMI*](gloss-p.md) è costituito da un file Managed Object Format (MOF) e da un file dll. Il file MOF definisce le classi per le quali l'implementazione del provider fornisce i dati.

Le definizioni delle classi MOF vengono compilate dall'utilità [**mofcomp**](mofcomp.md) e archiviate nel [*repository WMI*](gloss-w.md), noto anche come repository Common Information Model (CIM). Un modo meno comune per creare classi consiste nell'usare i metodi dell' [API com per WMI](com-api-for-wmi.md).

> [!Note]  
> Per assicurarsi che tutte le definizioni di classe WMI per gli oggetti gestiti vengano ripristinate nel [*repository WMI*](gloss-w.md) se WMI presenta un errore e viene riavviato, usare l'istruzione del preprocessore [**\# pragma autocover**](pragma-autorecover.md) nel file MOF.

 

Le sezioni seguenti sono illustrate in questo argomento:

-   [Definizione degli oggetti da gestire](#defining-the-objects-to-manage)
-   [Definizione di proprietà o metodi](#defining-properties-or-methods)
-   [Correlazione tra oggetti](#relating-objects-to-each-other)
-   [Argomenti correlati](#related-topics)

## <a name="defining-the-objects-to-manage"></a>Definizione degli oggetti da gestire

Dopo aver identificato la parte dell'organizzazione da gestire, definire gli oggetti da gestire. La definizione deve includere i dati necessari e consente di implementare accuratamente le regole business pertinenti. È possibile definire oggetti a livello granulare, ma è preferibile decidere tra il livello di dettaglio contenuto nella definizione e la necessità di fornire dettagli sufficienti per essere utili. I collegamenti nelle fasi iniziali del processo possono risparmiare tempo, ma potrebbero causare un maggiore lavoro in futuro.

L'esercitazione CIM nel sito Web Distributed Management Task Force (DMTF) contiene informazioni ottimali sul processo di progettazione. Per ulteriori informazioni, vedere [www.DMTF.org](https://www.dmtf.org/).

Quando si sviluppa e si implementa una progettazione dello schema, tenere presenti i seguenti fattori:

-   Qualificatori

    I qualificatori forniscono informazioni su come descrivere classi, oggetti, proprietà, metodi e parametri. e vengono applicati alle definizioni di classi e proprietà. Nel codice MOF i qualificatori sono racchiusi tra parentesi quadre e possono includere la \[ chiave \] o l' \[ associazione \] . Per ulteriori informazioni, vedere [aggiunta di un qualificatore](adding-a-qualifier.md) e [qualificatori WMI](wmi-qualifiers.md).

-   Spazio dei nomi

    Uno spazio dei nomi è un'unità logica per raggruppare classi e oggetti, nonché l'ambito e la visibilità del controllo. In genere, uno spazio dei nomi contiene un set di classi e oggetti che rappresentano oggetti gestiti in un ambiente specifico. Per ulteriori informazioni, vedere [creazione di gerarchie all'interno di WMI](creating-hierarchies-within-wmi.md).

-   Oggetto

    Un oggetto modellato può essere un elemento fisico o logico dello schema. Ad esempio, è possibile modellare un'unità disco fisica, ad esempio un'unità disco rigido, o un disco logico che può essere una partizione su un disco fisico. Una progettazione che utilizza una classe per modellare un'unità disco fisica e quindi estende tale classe per modellare un disco logico è più estendibile di quella che tenta di creare una classe separata per ogni tipo di disco.

-   Data

    I dati possono essere dinamici o statici. Se i dati sono dinamici, è necessario creare un provider di classi per l'oggetto.

    Per consentire all'utente di modificare i dati, è necessario determinare se si desidera che una proprietà sia direttamente scrivibile o modificabile solo utilizzando un metodo chiamato dall'utente.

## <a name="defining-properties-or-methods"></a>Definizione di proprietà o metodi

In genere, una proprietà della classe WMI è simile a una proprietà in una classe C++. Se le uniche azioni implementate dal codice per i dati sono l'ottenimento del valore o l'impostazione del valore, i dati devono essere definiti come proprietà della classe WMI.

Un metodo WMI esegue in genere un'azione che modifica lo stato di un oggetto gestito. Se, ad esempio, l'azione prevede l'abilitazione o la disabilitazione dell'operazione di un oggetto hardware, un metodo è probabilmente preferibile alla creazione di una proprietà di lettura/scrittura. È anche possibile decidere di creare una proprietà che visualizza lo stato dell'hardware.

Quando si crea una classe o un'istanza di, è possibile includere commenti. Usare questa tecnica per documentare la classe o spiegare le tecniche di programmazione. Per ulteriori informazioni, vedere [creazione di un commento](creating-a-comment.md). Inoltre, è possibile aggiungere dati per qualificare lo scopo di un oggetto dati. Per ulteriori informazioni, vedere [aggiunta di un qualificatore](adding-a-qualifier.md).

## <a name="relating-objects-to-each-other"></a>Correlazione tra oggetti

Esistono due modi per correlare gli oggetti tra loro: creando oggetti separati e un oggetto di associazione che li mette in correlazione o incorporando un oggetto nell'altro. CIM non supporta gli oggetti incorporati, pertanto è necessario utilizzare il primo metodo per essere conforme a CIM. Tuttavia, WMI supporta oggetti incorporati, quindi utilizzare uno di questi metodi per rappresentare una relazione tra oggetti. È possibile trovare esempi di oggetti incorporati nelle [classi Win32](/windows/desktop/CIMWin32Prov/win32-provider). Ad esempio, [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) ha l'oggetto incorporato [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace), che ha un altro oggetto incorporato [**, \_ trustee Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee).

Quando si decide come rappresentare le relazioni tra oggetti, tenere presente quanto segue:

-   Se un'istanza è utile da sola, un'associazione funziona in modo ottimale. Ad esempio, [**Win32 \_ Process**](/windows/desktop/CIMWin32Prov/win32-process) e [**Win32 \_ AccountUtente**](/windows/desktop/CIMWin32Prov/win32-useraccount). Per ulteriori informazioni, vedere [dichiarazione di una classe di associazione](declaring-an-association-class.md).
-   Se un'istanza non esiste all'esterno dell'oggetto padre, un oggetto incorporato funziona in modo ottimale. Ad esempio [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) e [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace). Per altre informazioni, vedere [incorporamento di oggetti in una classe](embedded-objects.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di un provider WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Invio di dati a WMI](providing-data-to-wmi.md)
</dt> <dt>

[Tipi di dati MOF](mof-data-types.md)
</dt> </dl>

 

 
