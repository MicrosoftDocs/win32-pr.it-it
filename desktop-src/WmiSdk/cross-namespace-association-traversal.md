---
description: A partire da Windows 7, Strumentazione gestione Windows (WMI) ha implementato un meccanismo standard per individuare i profili mediante lo schema CIM.
ms.assetid: e748b623-5ff3-464d-ba09-96cf226de7b6
ms.tgt_platform: multiple
title: Attraversamento dell'associazione tra spazi dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fe2bbb408c4d89a7093adf45f3daf276df294ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880673"
---
# <a name="cross-namespace-association-traversal"></a>Attraversamento dell'associazione tra spazi dei nomi

A partire da Windows 7, Strumentazione gestione Windows (WMI) ha implementato un meccanismo standard per individuare i profili mediante lo schema CIM.

WMI supporta l'attraversamento dell'associazione tra spazi dei nomi e la registrazione del profilo di associazione. Per ulteriori informazioni sulla registrazione del profilo e sull'implementazione standard CIM dell'attraversamento delle associazioni, vedere DSP1033 ( [https://www.dmtf.org/standards/published\_documents/DSP1033.pdf](https://www.dmtf.org/sites/default/files/standards/documents/DSP1033_1.0.0.pdf) ).

Per supportare questa funzionalità, l'infrastruttura WMI ha fatto quanto segue:

-   Creazione dello spazio dei nomi Interop: \\ \\ interoperabilità radice.
-   Attraversamento dell'associazione tra spazi dei nomi consentiti. Le associazioni che incrociano gli spazi dei nomi supportano il filtro a livello di classe di associazione e a livello di spazio dei nomi implementato.
-   Sono state aggiunte le classi CIM [**\_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)), [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)e [**CIM \_ ReferencedProfile**](cim-referencedprofile.md) .
-   Compatibilità 2.17.1 della versione dello schema CIM implementata. Per ulteriori informazioni, vedere [CIM schema Compatibility](cim-schema-compatibility.md).

## <a name="interop-namespace"></a>Spazio dei nomi Interop

Lo spazio dei nomi Interop fornisce un percorso comune per l'individuazione da parte di un'applicazione client di tutti i profili supportati in un computer. I profili possono essere usati per gestire vari aspetti di un sistema operativo, di un array di archiviazione o di un database.

Tutti gli oggetti e le classi di interoperabilità devono essere definiti nello \\ spazio dei nomi interoperabilità radice.

## <a name="cim-classes"></a>Classi CIM

Le classi CIM descritte nell'elenco seguente supportano l'attraversamento dell'associazione tra spazi dei nomi.

<dl> <dt>

<span id="CIM_RegisteredProfile"></span><span id="cim_registeredprofile"></span><span id="CIM_REGISTEREDPROFILE"></span>[**\_REGISTEREDPROFILE CIM**](/previous-versions//ee309375(v=vs.85))
</dt> <dd>

Utilizzato per identificare la specifica del profilo che viene annunciata come implementata. Questa classe specifica le informazioni che includono il nome del profilo, l'organizzazione e la versione con cui è conforme l'implementazione.

</dd> <dt>

<span id="CIM_ElementConformsToProfile"></span><span id="cim_elementconformstoprofile"></span><span id="CIM_ELEMENTCONFORMSTOPROFILE"></span>[**\_ELEMENTCONFORMSTOPROFILE CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dd>

Utilizzato per associare istanze di elementi di gestione definiti nei profili con la classe [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) che identifica le specifiche specifiche del profilo implementate.

</dd> <dt>

<span id="CIM_ReferencedProfile"></span><span id="cim_referencedprofile"></span><span id="CIM_REFERENCEDPROFILE"></span>[**\_REFERENCEDPROFILE CIM**](cim-referencedprofile.md)
</dt> <dd>

Utilizzato per rappresentare la relazione tra profili.

</dd> </dl>

## <a name="implementing-cross-namespace-association-traversal"></a>Implementazione dell'attraversamento di associazioni tra spazi dei nomi

Il servizio WMI consente l'attraversamento dell'associazione tra spazi dei nomi. WMI fornisce lo spazio dei nomi di interoperabilità per registrare i profili e associarli a profili implementati in spazi dei nomi diversi. Tuttavia, per usare l'attraversamento dell'associazione, gli implementatori devono creare un'istanza delle classi di profilo sia nell'interoperabilità che nello spazio dei nomi implementato. Per ulteriori informazioni, vedere [scrittura di un provider di associazioni per l'interoperabilità](writing-an-association-provider-for-interop.md).

Le associazioni che incrociano gli spazi dei nomi all'interno dello stesso ambiente di gestione devono essere create in entrambi gli spazi dei nomi di interoperabilità e implementato. In caso contrario, l'attraversamento dell'associazione non funzionerà. Ad esempio, il provider di associazioni Power profile deve essere registrato con gli spazi dei nomi root/Interop e root/cimv2/Power. L'attraversamento dell'associazione dovrebbe essere in grado di essere eseguito da uno spazio dei nomi all'altro. Per esempi di attraversamento delle associazioni, vedere [accesso ai dati nello spazio dei nomi Interop](accessing-data-in-the-interop-namespace.md).

* * Windows Vista: * *

Dopo l'aggiornamento a Windows 7, se sono presenti profili di dispositivo di interoperabilità precedentemente installati nello spazio dei nomi radice/interoperabilità, non verrà installato alcun profilo di Windows 7. Questi oggetti profilo di terze parti sovrascrivono lo schema di interoperabilità di Windows 7 per mantenere la funzionalità. Inoltre, viene registrato l'evento dell'applicazione WMI con ID 5631.

Per ottenere i profili di interoperabilità di Windows 7, è necessario compilare la versione di Windows 7 del file Interop. mof e i file MFL correlati. Per ulteriori informazioni, vedere [compilazione di file MOF](compiling-mof-files.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**\_REGISTEREDPROFILE CIM**](/previous-versions//ee309375(v=vs.85))
</dt> <dt>

[**\_ELEMENTCONFORMSTOPROFILE CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dt>

[**\_REFERENCEDPROFILE CIM**](cim-referencedprofile.md)
</dt> <dt>

[Compatibilità con lo schema CIM](cim-schema-compatibility.md)
</dt> <dt>

[Scrittura di un provider di associazioni per l'interoperabilità](writing-an-association-provider-for-interop.md)
</dt> <dt>

[Accesso ai dati nello spazio dei nomi Interop](accessing-data-in-the-interop-namespace.md)
</dt> </dl>

 

 
