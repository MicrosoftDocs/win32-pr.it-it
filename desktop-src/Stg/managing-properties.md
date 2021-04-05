---
title: Gestione delle proprietà
description: Ogni proprietà è costituita da un identificatore di proprietà (univoco all'interno del set di proprietà), da un tag di tipo Variant (VT o VarType) che rappresenta il tipo di un valore e dal valore stesso.
ms.assetid: d220ecb4-b014-4ac9-a636-9a493187cc87
keywords:
- Archiviazione strutturata Strctd STG, uso, gestione delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10dd78a1f8a8484090728dba6fe149840e940461
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872649"
---
# <a name="managing-properties"></a>Gestione delle proprietà

Ogni proprietà è costituita da un *identificatore di proprietà* (univoco all'interno del set di proprietà), da un *tag di tipo Variant (VT o VarType)* che rappresenta il tipo di un valore e dal *valore* stesso. Il tag di tipo Variant descrive la rappresentazione dei dati nel valore. Inoltre, a una proprietà può essere assegnato un *nome di stringa* che può essere usato per identificare la proprietà, anziché usare l'identificatore di proprietà numerico (ID) obbligatorio. Per creare e gestire le proprietà, COM definisce l'interfaccia [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) .

L'interfaccia [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) include metodi per la lettura e la scrittura di matrici di proprietà o nomi di proprietà. L'interfaccia include metodi di [**commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) e [**ripristino**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) simili a metodi [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) con lo stesso nome. Sono disponibili metodi di utilità che consentono di impostare l'identificatore di classe (CLSID) del set di proprietà, impostare le ore associate al set e ottenere le statistiche relative al set di proprietà. Infine, il metodo [**enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) crea un enumeratore e restituisce un puntatore alla relativa interfaccia [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) . È possibile chiamare i metodi di questa interfaccia per enumerare le strutture [**Campo STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) sull'oggetto, in modo da fornire informazioni su tutte le proprietà nel set di proprietà corrente.

Di seguito è riportato un esempio di come vengono rappresentate le proprietà. Se una proprietà specifica in un set di proprietà include il nome scientifico di un animale, tale nome può essere archiviato come stringa con terminazione zero. Memorizzato insieme al nome sarebbe un indicatore di tipo per indicare che il valore è una stringa con terminazione zero. Queste proprietà possono avere le seguenti caratteristiche:



| ID proprietà | Identificatore di stringa | Indicatore del tipo | Valore rappresentato              |
|-------------|-------------------|----------------|--------------------------------|
| 02          | PID \_ animalname   | \_LPWSTR VT     | Stringa Unicode con terminazione zero |
| 03          | \_LEGCOUNT PID     | \_I2 VT         | WORD                           |



 

Qualsiasi applicazione che riconosce il formato del set di proprietà, che lo identifica tramite il relativo identificatore di formato (FMTID), può esaminare la proprietà con un identificatore di PID \_ animalname, determinare che si tratta di una stringa con terminazione zero, quindi leggere e scrivere il valore. Sebbene l'applicazione sia in grado di chiamare [**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) per leggere uno o tutti i set di proprietà (ottenendo prima un puntatore), è necessario che l'applicazione sappia come interpretare il set di proprietà.

Il valore di una proprietà viene passato tramite le interfacce di proprietà come istanza del tipo [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).

È importante distinguere tra queste proprietà archiviate (persistenti) e le proprietà della fase di esecuzione. Le costanti con valori di tipo Variant hanno nomi che iniziano con VT \_ . Il set di PROPVARIANTs validi, tuttavia, non è interamente equivalente al set di varianti usato nei controlli ActiveX e di automazione.

L'unica differenza tra le due strutture è il set consentito di Tag VT \_ (tipo Variant/VARTYPE) in ognuno di essi. Se un determinato tipo di proprietà può essere usato sia in una variante che in un PROPVARIANT, il tag del tipo (il \_ valore VT) ha sempre un valore identico. Per un determinato valore VT, inoltre, \_ la rappresentazione in memoria usata nelle varianti e PROPVARIANTs è identica. Insieme, questo approccio consente al sistema di tipi di intercettare i tag dei tipi non consentiti, mentre allo stesso tempo consente a un client esperto di implementare un cast del puntatore quando appropriato.

Per ulteriori informazioni, vedere la sezione seguente [considerazioni sull'archiviazione delle proprietà](property-storage-considerations.md).

 

 