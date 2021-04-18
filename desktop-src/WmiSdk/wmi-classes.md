---
description: In questa sezione vengono fornite informazioni sulla classe WMI e sulla pagina di riferimento.
ms.assetid: 0110677a-bbba-42f7-8e59-55d83758f70a
ms.tgt_platform: multiple
title: Classi WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa764d39c1fb048e125898a1f7e6d5cadf7f127d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310340"
---
# <a name="wmi-classes"></a>Classi WMI

In questa sezione vengono fornite informazioni sulla classe WMI e sulla pagina di riferimento. Per ulteriori informazioni su come recuperare i dati di una classe o un'istanza, vedere [modifica delle informazioni sulle classi e sulle istanze](manipulating-class-and-instance-information.md). L'elenco seguente elenca, descrive e fornisce collegamenti a informazioni specifiche sulle classi WMI. Per ulteriori informazioni ed esempi di codice di script sull'utilizzo delle classi WMI per ottenere un'ampia gamma di dati di sistema operativo e hardware, vedere [attività WMI per script e applicazioni](wmi-tasks-for-scripts-and-applications.md). Per esempi di C++, vedere [esempi di applicazioni WMI c++](wmi-c---application-examples.md). La [connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md) Mostra come ottenere i dati remoti. È anche possibile usare PowerShell per accedere a oggetti WMI. per un elenco delle classi WMI che includono esempi di codice PowerShell, vedere [qui](https://msdn.microsoft.com/library/tags-cloud.aspx?tag=powershell+code+wmi).



| Sezione                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Classi di sistema WMI](wmi-system-classes.md)               | Classi predefinite incluse in ogni spazio dei nomi nel Strumentazione gestione Windows (WMI) Core. È possibile riconoscere una classe di sistema WMI perché il nome inizia con un doppio carattere di sottolineatura ( \_ \_ ). Queste classi forniscono gran parte delle funzionalità di base di WMI. Le classi di sistema WMI sono simili in funzione alle tabelle di sistema in SQL Server. |
| [Classi MSFT](msft-classes.md)                           | Altre classi Microsoft che offrono i mezzi per modificare diverse funzionalità del sistema operativo, ad esempio gli eventi remoti e le estensioni dei criteri. Le classi di [risoluzione dei problemi WMI](wmi-troubleshooting.md) sono classi MSFT che forniscono dati sulle operazioni WMI.                                                                                               |
| [Classi CIM](cimclas.md)                                 | Classi dello schema [*Common Information Model (CIM)*](gloss-c.md) . Se si desidera scrivere classi WMI personalizzate, è possibile ereditare da una o più di queste classi. Le [classi Win32](/windows/desktop/CIMWin32Prov/win32-provider) WMI ereditano dalle classi CIM.                                                                          |
| [Classi consumer standard](standard-consumer-classes.md) | Set di consumer di eventi WMI che attivano un'azione alla ricezione di un evento arbitrario. Per ulteriori informazioni, vedere [monitoraggio degli eventi](monitoring-events.md).                                                                                                                                                                                               |



 

## <a name="wmi-class-scripting-center-code-examples"></a>Esempi di codice di classe WMI Scripting Center

Gli esempi di codice di Scripting Center seguenti influiscono su più classi WMI in più spazi dei nomi.



| Collegamento                                                                                                                                      | Descrizione                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Interfaccia utente grafica WMI Explorer e metodo WMI Generator](https://Gallery.TechNet.Microsoft.Com/scriptcenter/89c759b7-20b4-49e8-98a8-3c8fbdb2dd69) | Script di esempio che fornisce una GUI WMI Explorer e il metodo WMI helper.                                                                                                                                                        |
| [Esplora WMI cerca gli spazi dei nomi WMI](https://Gallery.TechNet.Microsoft.Com/scriptcenter/WMI-Explorer-Search-WMI-cd87e309)                 | Consente agli utenti di cercare le classi in tutti gli spazi dei nomi disponibili sui computer specificati. Questo esempio è la riga di comando versione dell'esempio GUI WMI Explorer e può essere considerata un'estensione di Get-WmiObject-List. |
| [Strumento di amministrazione del sistema Windows Arposh](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Arposh-Windows-System-a1beb102)            | AWSA è stato creato tenendo presente l'amministratore di sistema. La risoluzione dei problemi di Windows richiede una vasta gamma di strumenti e informazioni. AWSA unisce questi strumenti in un'unica posizione centrale e aggiunge funzionalità aggiuntive.       |



 

## <a name="naming-conventions-for-wmi-classes-and-properties"></a>Convenzioni di denominazione per classi e proprietà WMI

I nomi delle proprietà devono essere conformi alla sintassi Managed Object Format (MOF) definita da Distributed Management Task Force (DTMF). I caratteri dell'identificatore iniziale devono essere tra le lettere da a a z e il carattere di sottolineatura ( \_ ). Tutti i caratteri aggiuntivi devono essere tra le lettere dalla a alla z, il carattere di sottolineatura e i numeri da 0 a 9. Per ulteriori informazioni, vedere la sezione Utilizzo Unicode della [specifica CIM versione 2,2](https://www.dmtf.org/standards/cim).

Le parole riservate di SQL non devono essere usate nei nomi di classi e proprietà. Per un elenco completo delle parole riservate SQL e per altre informazioni, vedere la sezione linee guida della [specifica CIM versione 2,2](https://www.dmtf.org/standards/cim).

## <a name="document-conventions-for-a-wmi-class-reference-page"></a>Convenzioni documento per una pagina di riferimento della classe WMI

In questa sezione vengono identificate e descritte le convenzioni dei documenti per una pagina di riferimento della classe WMI.

Una tipica pagina di riferimento contiene un blocco di sintassi, una tabella dei metodi e un elenco delle proprietà.

-   Blocco di sintassi

    Versione semplificata del codice MOF che include il nome della classe, la classe padre (se presente) e le proprietà della classe in ordine alfabetico con i tipi di dati.

-   Tabella Methods

    Se una classe dispone di metodi, i metodi vengono elencati nella tabella immediatamente dopo il blocco della sintassi. Ogni metodo implementato è collegato a una pagina di riferimento.

-   Elenco delle proprietà

    Ogni proprietà della classe è elencata con un tipo di dati, un tipo di accesso (di sola lettura o di lettura/scrittura), qualificatori e una descrizione della proprietà.

## <a name="syntax-block"></a>Blocco di sintassi

``` syntax
class Win32_xyz : CIM_xyz 
{
  uint16 abc  ;
  string def  ;
};
```

## <a name="methods-table"></a>Tabella Methods



| \_Metodi Win32 XYZ | Descrizione                                |
|--------------------|--------------------------------------------|
| *SomeMethod*       | Breve descrizione dell'operazione eseguita dal metodo. |



 

## <a name="properties-list"></a>Elenco delle proprietà

<dl> <dt>

<span id="abc"></span><span id="ABC"></span>ABC
</dt> <dd>

Tipo di dati: **UInt16**

Tipo di accesso: indica se si dispone dell'accesso in lettura/scrittura o in sola lettura a questa proprietà.

Qualificatori: se presente, Mostra i qualificatori per la proprietà. Ad esempio, **Key**, **override**.

Descrive la proprietà e fornisce informazioni sull'ereditarietà per la proprietà. Ad esempio, questa proprietà viene ereditata da ** \_ CIM* XYZ * * *. Esiste un collegamento alla classe padre se Microsoft fornisce un'implementazione di tale classe. Tuttavia, le classi CIM non sono disponibili.

</dd> <dt>

<span id="def"></span><span id="DEF"></span>def
</dt> <dd>

Tipo di dati: **String**

Tipo di accesso: sola lettura

Descrizione della proprietà.

</dd> </dl>

## <a name="remarks"></a>Commenti

Fornisce ulteriori informazioni sulla classe, se applicabile. Fornisce inoltre informazioni sulla derivazione, se applicabile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su WMI](wmi-reference.md)
</dt> </dl>

 

 
