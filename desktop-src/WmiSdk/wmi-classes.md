---
description: In questa sezione vengono fornite informazioni sulla classe WMI e sulla pagina di riferimento.
ms.assetid: 0110677a-bbba-42f7-8e59-55d83758f70a
ms.tgt_platform: multiple
title: Classi WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1da15af60f1d1a32d652c8776e20ef36d65c1ff158dc6ac7465886361c5862c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757511"
---
# <a name="wmi-classes"></a>Classi WMI

In questa sezione vengono fornite informazioni sulla classe WMI e sulla pagina di riferimento. Per altre informazioni su come recuperare i dati della classe o dell'istanza, vedere Modifica delle informazioni sulla [classe e sull'istanza](manipulating-class-and-instance-information.md). L'elenco seguente elenca, descrive e fornisce collegamenti a informazioni specifiche sulla classe WMI. Per altre informazioni ed esempi di codice script sull'uso delle classi WMI per ottenere un'ampia gamma di dati hardware e del sistema operativo, vedere [Attività WMI per](wmi-tasks-for-scripts-and-applications.md)script e applicazioni . Per esempi in C++, vedere [Esempi di applicazioni C++ WMI](wmi-c---application-examples.md). [La connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md) illustra come ottenere dati remoti. È anche possibile usare PowerShell per accedere agli oggetti WMI. Per un elenco delle classi WMI che includono esempi di codice di PowerShell, vedere [qui](https://msdn.microsoft.com/library/tags-cloud.aspx?tag=powershell+code+wmi).



| Sezione                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Classi di sistema WMI](wmi-system-classes.md)               | Classi predefinite incluse in ogni spazio dei nomi nel core Windows Management Instrumentation (WMI). È possibile riconoscere una classe di sistema WMI perché il nome inizia con un doppio carattere di sottolineatura ( \_ \_ ). Queste classi forniscono gran parte delle funzionalità di base per WMI. Le classi di sistema WMI sono simili allo scopo delle tabelle di sistema in SQL server. |
| [Classi MSFT](msft-classes.md)                           | Altre classi Microsoft che offrono i mezzi per modificare diverse funzionalità del sistema operativo, ad esempio eventi remoti ed estensioni dei criteri. Le [classi di risoluzione dei](wmi-troubleshooting.md) problemi WMI sono classi MSFT che forniscono dati sulle operazioni WMI.                                                                                               |
| [Classi CIM](cimclas.md)                                 | [*Common Information Model (CIM).*](gloss-c.md) Se si vogliono scrivere classi WMI personalizzate, è possibile ereditare da una o più di queste classi. Le classi [Win32](/windows/desktop/CIMWin32Prov/win32-provider) WMI ereditano dalle classi CIM.                                                                          |
| [Classi consumer standard](standard-consumer-classes.md) | Set di consumer di eventi WMI che attivano un'azione alla ricezione di un evento arbitrario. Per altre informazioni, vedere [Monitoraggio degli eventi](monitoring-events.md).                                                                                                                                                                                               |



 

## <a name="wmi-class-scripting-center-code-examples"></a>Esempi di codice di Scripting Center per classi WMI

Gli esempi di codice di Scripting Center seguenti influiscono su più classi WMI in più spazi dei nomi.



| Collegamento                                                                                                                                      | Descrizione                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [GUI WMI Explorer and WMI Method Help Generator](https://Gallery.TechNet.Microsoft.Com/scriptcenter/89c759b7-20b4-49e8-98a8-3c8fbdb2dd69) | Script di esempio che fornisce un'interfaccia utente grafica wmi explorer e un generatore di guida del metodo WMI.                                                                                                                                                        |
| [WMI Explorer Search WMI NameSpaces](https://Gallery.TechNet.Microsoft.Com/scriptcenter/WMI-Explorer-Search-WMI-cd87e309)                 | Consente agli utenti di cercare classi in tutti gli spazi dei nomi disponibili nei computer specificati. Questo esempio è il verison della riga di comando dell'esempio di Esplora WMI dell'interfaccia utente grafica e può essere considerato un'estensione di Get-WmiObject -List. |
| [Strumento di amministrazione Windows Arposh](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Arposh-Windows-System-a1beb102)            | AWSA è stato creato con l'amministratore di sistema in mente. La Windows dei problemi richiede una vasta gamma di strumenti e conoscenze. AWSA riunisce questi strumenti in un'unica posizione centrale e aggiunge funzionalità aggiuntive.       |



 

## <a name="naming-conventions-for-wmi-classes-and-properties"></a>Convenzioni di denominazione per le classi e le proprietà WMI

I nomi delle proprietà devono essere conformi alla Managed Object Format (MOF) definita da Distributed Management Task Force (DTMF). I caratteri dell'identificatore iniziale devono essere tratti dalle lettere da a a z e dal carattere di sottolineatura ( \_ ). Tutti i caratteri aggiuntivi devono essere dalle lettere da a a z, dal carattere di sottolineatura e dai numeri da 0 a 9. Per altre informazioni, vedere la sezione Utilizzo Unicode della specifica [CIM versione 2.2.](https://www.dmtf.org/standards/cim)

SQL le parole riservate non devono essere usate nei nomi di classi e proprietà. Per un elenco completo delle SQL parole riservate e per altre informazioni, vedere la sezione Linee guida della specifica [CIM versione 2.2.](https://www.dmtf.org/standards/cim)

## <a name="document-conventions-for-a-wmi-class-reference-page"></a>Convenzioni di documento per una pagina di riferimento della classe WMI

Questa sezione identifica e descrive le convenzioni del documento per una pagina di riferimento della classe WMI.

Una tipica pagina di riferimento contiene un blocco di sintassi, una tabella dei metodi e un elenco di proprietà.

-   Blocco di sintassi

    Versione semplificata del codice MOF che include il nome della classe, la classe padre (se presente) e le proprietà della classe, in ordine alfabetico, con tipi di dati.

-   Tabella Metodi

    Se una classe dispone di metodi, i metodi vengono elencati nella tabella immediatamente dopo il blocco di sintassi. Ogni metodo implementato è collegato a una pagina di riferimento.

-   Elenco delle proprietà

    Ogni proprietà della classe è elencata con un tipo di dati, un tipo di accesso (sola lettura o lettura/scrittura), qualificatori e una descrizione della proprietà.

## <a name="syntax-block"></a>Blocco di sintassi

``` syntax
class Win32_xyz : CIM_xyz 
{
  uint16 abc  ;
  string def  ;
};
```

## <a name="methods-table"></a>Tabella Metodi



| Metodi xyz Win32 \_ | Descrizione                                |
|--------------------|--------------------------------------------|
| *SomeMethod*       | Breve descrizione delle attività del metodo. |



 

## <a name="properties-list"></a>Elenco delle proprietà

<dl> <dt>

<span id="abc"></span><span id="ABC"></span>Abc
</dt> <dd>

Tipo di dati: **uint16**

Tipo di accesso: indica se si dispone dell'accesso in lettura/scrittura o di sola lettura a questa proprietà.

Qualificatori: se presenti, visualizza i qualificatori per la proprietà. Ad esempio, **Chiave**, **Eseguire l'override di**.

Descrive la proprietà e fornisce informazioni sull'ereditarietà per la proprietà. Ad esempio, questa proprietà viene ereditata da **CIM \_* xyz***. Esiste un collegamento alla classe padre se Microsoft fornisce un'implementazione di tale classe. Tuttavia, le classi CIM non sono disponibili.

</dd> <dt>

<span id="def"></span><span id="DEF"></span>Def
</dt> <dd>

Tipo di dati: **stringa**

Tipo di accesso: sola lettura

Descrizione della proprietà.

</dd> </dl>

## <a name="remarks"></a>Commenti

Fornisce altre informazioni sulla classe, se applicabile. Fornisce anche informazioni sulla derivazione, se applicabile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su WMI](wmi-reference.md)
</dt> </dl>

 

 
