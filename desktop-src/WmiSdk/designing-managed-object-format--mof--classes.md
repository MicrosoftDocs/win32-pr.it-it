---
description: Un provider WMI è costituito da un file Managed Object Format (MOF) e da un file DLL. Il file MOF definisce le classi per le quali l'implementazione del provider fornisce i dati.
ms.assetid: 20ef6b88-2aaa-4e86-bc4a-bebc34069672
ms.tgt_platform: multiple
title: Progettazione di Managed Object Format (MOF)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 78e761b5fe0b7eeee80dc3188ba952812fb1d7f0bad963452a23e9073bb34282
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119374671"
---
# <a name="designing-managed-object-format-mof-classes"></a>Progettazione di Managed Object Format (MOF)

Un [*provider WMI*](gloss-p.md) è costituito da un file Managed Object Format (MOF) e da un file DLL. Il file MOF definisce le classi per le quali l'implementazione del provider fornisce i dati.

Le definizioni delle classi MOF vengono compilate dall'utilità [**mofcomp**](mofcomp.md) e archiviate nel [*repository WMI,*](gloss-w.md)noto anche come repository Common Information Model (CIM). Un modo meno comune per creare classi è tramite i metodi [dell'API COM per WMI.](com-api-for-wmi.md)

> [!Note]  
> Per assicurarsi che tutte le definizioni di classe WMI per gli oggetti gestiti siano ripristinate nel [*repository WMI*](gloss-w.md) se WMI presenta un errore e si riavvia, usare l'istruzione del preprocessore [**\# pragma autorecover**](pragma-autorecover.md) nel file MOF.

 

In questo argomento vengono illustrate le sezioni seguenti:

-   [Definizione degli oggetti da gestire](#defining-the-objects-to-manage)
-   [Definizione di proprietà o metodi](#defining-properties-or-methods)
-   [Relazione tra oggetti](#relating-objects-to-each-other)
-   [Argomenti correlati](#related-topics)

## <a name="defining-the-objects-to-manage"></a>Definizione degli oggetti da gestire

Dopo aver identificato la parte dell'azienda da gestire, definire gli oggetti da gestire. La definizione deve includere i dati necessari e consentire l'implementazione accurata delle regole business pertinenti. È possibile definire oggetti a un livello granulare, ma è meglio decidere tra il livello di dettaglio contenuto nella definizione e la necessità di fornire dettagli sufficienti per essere utili. I tasti di scelta rapida nelle prime fasi del processo possono risparmiare tempo, ma potrebbero causare più lavoro in futuro.

L'esercitazione CIM nel sito Web DmTF (Distributed Management Task Force) contiene informazioni eccellenti sul processo di progettazione. Per altre informazioni, vedere [www.dmtf.org](https://www.dmtf.org/).

Quando si sviluppa e implementa una progettazione dello schema, tenere presenti i fattori seguenti:

-   Qualificatori

    I qualificatori forniscono informazioni su come descrivere classi, oggetti, proprietà, metodi e parametri. e vengono applicati alle definizioni di classi e proprietà. Nel codice MOF i qualificatori sono racchiusi tra parentesi quadre e possono includere \[ la chiave \] o \[ l'associazione \] . Per altre informazioni, vedere [Aggiunta di un qualificatore](adding-a-qualifier.md) e [di qualificatori WMI.](wmi-qualifiers.md)

-   Spazio dei nomi

    Uno spazio dei nomi è un'unità logica per raggruppare classi e oggetti e controllare l'ambito e la visibilità. In genere, uno spazio dei nomi contiene un set di classi e oggetti che rappresentano oggetti gestiti in un ambiente specifico. Per altre informazioni, vedere Creazione [di gerarchie all'interno di WMI.](creating-hierarchies-within-wmi.md)

-   Oggetto

    Un oggetto modellato può essere un elemento fisico o logico dello schema. Ad esempio, è possibile modellare un'unità disco fisica, ad esempio un'unità disco rigido, o un disco logico che può essere una partizione in un disco fisico. Una progettazione che usa una classe per modellare un'unità disco fisica e quindi estende tale classe per modellare un disco logico è più estendibile di una classe che tenta di creare una classe separata per ogni tipo di disco.

-   Dati

    I dati possono essere dinamici o statici. Se i dati sono dinamici, è necessario creare un provider di classi per i dati.

    Per consentire all'utente di modificare i dati, è necessario determinare se si desidera che una proprietà sia direttamente scrivibile o modificabile solo usando un metodo chiamato dall'utente.

## <a name="defining-properties-or-methods"></a>Definizione di proprietà o metodi

In genere, una proprietà della classe WMI è simile a una proprietà in una classe C++. Se le uniche azioni implementate dal codice per la parte di dati sono ottenere il valore o impostare il valore, i dati devono essere definiti come proprietà della classe WMI.

Un metodo WMI esegue in genere un'azione che modifica lo stato di un oggetto gestito. Ad esempio, se l'azione è abilitare o disabilitare il funzionamento di un oggetto hardware, un metodo è probabilmente preferibile alla creazione di una proprietà di lettura/scrittura. È anche possibile decidere di creare una proprietà che visualizza lo stato dell'hardware.

Quando si crea una classe o un'istanza di , è possibile includere commenti. Usare questa tecnica per documentare la classe o illustrare le tecniche di programmazione. Per altre informazioni, vedere [Creazione di un commento.](creating-a-comment.md) Inoltre, è possibile aggiungere dati per qualificare lo scopo di un oggetto dati. Per altre informazioni, vedere Aggiunta [di un qualificatore.](adding-a-qualifier.md)

## <a name="relating-objects-to-each-other"></a>Relazione tra oggetti

Esistono due modi per correlare gli oggetti tra loro: creando oggetti separati e un oggetto di associazione che li mette in relazione o incorporando un oggetto nell'altro. CIM non supporta gli oggetti incorporati, pertanto per essere conforme a CIM è necessario usare il primo metodo. Wmi supporta tuttavia oggetti incorporati, pertanto utilizzare entrambi i metodi per rappresentare una relazione tra gli oggetti. È possibile trovare esempi di oggetti incorporati in [Classi Win32.](/windows/desktop/CIMWin32Prov/win32-provider) Ad esempio, [**\_ SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) ha l'oggetto [**incorporato Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace), che ha un altro oggetto incorporato, [**Win32 \_ Trustee.**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)

Quando si decide come rappresentare le relazioni tra oggetti, tenere presente quanto segue:

-   Se un'istanza è utile da sola, un'associazione funziona meglio. Ad esempio, [**Win32 \_ Process e**](/windows/desktop/CIMWin32Prov/win32-process) [**Win32 \_ UserAccount**](/windows/desktop/CIMWin32Prov/win32-useraccount). Per altre informazioni, vedere [Dichiarazione di una classe di associazione.](declaring-an-association-class.md)
-   Se un'istanza non esiste all'esterno dell'oggetto padre, un oggetto incorporato funziona meglio. Ad esempio, [**Win32 \_ SecurityDescriptor e**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace). Per altre informazioni, vedere [Incorporamento di oggetti in una classe](embedded-objects.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di un provider WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Fornire dati a WMI](providing-data-to-wmi.md)
</dt> <dt>

[Tipi di dati MOF](mof-data-types.md)
</dt> </dl>

 

 
