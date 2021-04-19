---
description: Le proprietà nelle classi WMI descrivono i dati relativi a un oggetto gestito.
ms.assetid: 4046bfc7-9528-4737-ad61-bbb8419d0b51
ms.tgt_platform: multiple
title: Aggiunta di una proprietà WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bba8944da155ca250edfed0c6e9160f555ba9551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317572"
---
# <a name="adding-a-wmi-property"></a>Aggiunta di una proprietà WMI

Le proprietà nelle classi WMI descrivono i dati relativi a un oggetto gestito. Ad esempio, **handle**, **ProcessID** e **PageFaults** vengono definiti come proprietà della classe [**di \_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) e descrivono gli aspetti di un processo del sistema operativo. Per ulteriori informazioni, vedere [scrittura di un provider di proprietà](writing-a-property-provider.md).

## <a name="defining-a-property-in-mof"></a>Definizione di una proprietà in MOF

Una proprietà WMI rappresenta un aspetto o uno stato nell'oggetto. Anziché creare metodi che ottengono e impostano semplicemente un valore, è possibile creare una proprietà. Ad esempio, la proprietà **NetEnabled** di [**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) Visualizza se lo stato dell'adapter è abilitato o disabilitato. Tuttavia, i metodi [**Enable**](/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter) e [**Disable**](/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter) eseguono effettivamente l'azione di modifica dello stato dell'adapter.

Una proprietà deve avere un tipo di dati. Il tipo di dati dell' **handle** della proprietà del [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) è **String** e il tipo di dati di **PageFaults** è **UInt32**. Se una proprietà può avere solo due Stati, il tipo di dati della proprietà è in genere impostato su **booleano**.

La proprietà può anche essere una matrice. Ad esempio, la proprietà ID di sicurezza (**SID**) di [**Win32 \_ trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) è una matrice di byte (**Uint8**) che contiene il SID. Le proprietà possono contenere oggetti incorporati che fanno riferimento a una o più istanze di un'altra classe WMI. Le proprietà dell'elenco di controllo di accesso discrezionale **(DACL)** e dell'elenco di controllo di accesso di sistema **(SACL)** di [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor), ad esempio, sono matrici di oggetti [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) che descrivono i gruppi e gli account che dispongono dell'accesso. La proprietà **Group** in **Win32 \_ securityDescriptor** contiene un riferimento a una singola istanza di **Win32 \_ trustee**. Per altre informazioni, vedere [incorporamento di oggetti in una classe](embedded-objects.md).

Una proprietà può avere diversi [*qualificatori*](gloss-q.md). Questi [qualificatori](wmi-qualifiers.md) possono essere [*Common Information Model (CIM)*](gloss-c.md) o qualificatori WMI oppure possono essere specifici di determinati tipi di classi, ad esempio, i qualificatori della classe del [contatore delle prestazioni](qualifiers-specific-to-wmi-performance-classes.md) . I qualificatori specificano un aspetto della proprietà, ad esempio se è di sola lettura o se non può essere modificato senza un privilegio specifico. Un'applicazione che tenta di scrivere nella proprietà **DACL** [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor), ad esempio, richiede i privilegi **SeSecurityPrivilege** e **SeRestorePrivilege**. Per ulteriori informazioni, vedere [aggiunta di un qualificatore](adding-a-qualifier.md).

Infine, una proprietà deve avere un nome. È possibile assegnare qualsiasi nome a una proprietà entro i limiti della procedura di programmazione standard. Tuttavia, esistono due eccezioni principali. In primo luogo, non è possibile usare una parola chiave MOF, ad esempio "class", come nome di proprietà. In secondo luogo, non è possibile utilizzare parole chiave WQL, ad esempio "Group", come nome di proprietà. Per ulteriori informazioni sulle parole chiave MOF e WQL, vedere [tipi di dati MOF](mof-data-types.md) e [WQL (SQL per WMI)](wql-sql-for-wmi.md).

Per il codice C++ e Managed Object Format (MOF), si dichiarano le proprietà di una classe nello stesso momento in cui viene dichiarata la classe.

**Per definire una proprietà**

-   Includere il tipo di dati della proprietà, il nome e un valore predefinito facoltativo e il qualificatore tra parentesi graffe della descrizione della classe.

    ``` syntax
    class MyClass 
    {
        [key] string   strProp;
        sint32         dwProp1 = 21;
        uint32         dwProp2;
    };
    ```

    La classe MyClass nell'esempio precedente presenta tre proprietà: una stringa di caratteri, un Signed Integer a 32 bit e un Unsigned Integer a 32 bit. A ogni proprietà viene assegnato un nome senza distinzione tra maiuscole e minuscole e un tipo di dati MOF.

    Il qualificatore [**chiave**](key-qualifier.md) definisce la proprietà di stringa come proprietà chiave che identifica in modo univoco un'istanza della classe. Per ulteriori informazioni sui qualificatori, vedere [aggiunta di un qualificatore](adding-a-qualifier.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una classe](creating-a-class.md)
</dt> </dl>

 

 
