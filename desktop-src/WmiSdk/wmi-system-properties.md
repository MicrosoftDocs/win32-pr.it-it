---
description: Windows Strumentazione gestione (WMI) definisce un set di proprietà di sistema associate a tutte le classi e istanze di classi.
ms.assetid: e812c0cb-3e08-4cac-8d05-2cd7abc922d1
ms.tgt_platform: multiple
title: Proprietà di sistema WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3471665e2e818037bb831c8d8ab39bbe0d56e01912afb1a3399b4055d3670a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120661"
---
# <a name="wmi-system-properties"></a>Proprietà di sistema WMI

Windows Strumentazione gestione (WMI) definisce un set di proprietà di sistema associate a tutte le classi e istanze di classi. Come per le classi di sistema, i nomi delle proprietà di sistema iniziano con un doppio carattere di sottolineatura, distinguendoli dalle proprietà create da applicazioni o provider che non devono iniziare con un carattere di sottolineatura singolo o doppio. Un altro modo per identificare una proprietà di sistema è usare il [**metodo IWbemClassObject::Get.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get)

Le proprietà di sistema sono disponibili in qualsiasi momento, ma i valori potrebbero essere **NULL.** **NULL** indica che una proprietà non si applica a un oggetto specifico. Tuttavia, le proprietà di sistema potrebbero non essere sempre disponibili per tutte le classi o le istanze.

## <a name="system-properties"></a>Proprietà di sistema

L'elenco seguente descrive le proprietà di sistema WMI. Gli esempi forniti sono tratto dalle proprietà di sistema della [**classe \_ OptionalFeature Win32,**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) descritte nella parte inferiore di questo argomento.

<dl> <dt>

<span id="__Class"></span><span id="__class"></span><span id="__CLASS"></span>**\_\_Classe**
</dt> <dd>

Tipo di dati: **CIM \_ STRING**

Tipo di accesso: sola lettura per le istanze. lettura/scrittura per le classi

Nome della classe.

Esempio: Win32 \_ OptionalFeature

</dd> <dt>

<span id="__Derivation"></span><span id="__derivation"></span><span id="__DERIVATION"></span>**\_\_Derivazione**
</dt> <dd>

Tipo di dati: **matrice CIM \_ STRING**

Tipo di accesso: sola lettura per istanze e classi

Gerarchia di classi della classe o dell'istanza corrente. Il primo elemento è la classe padre immediata, il successivo è l'elemento padre e così via. l'ultimo elemento è la classe di base.

Esempio: {CIM \_ LogicalElement, CIM \_ ManagedSystemElement}

</dd> <dt>

<span id="__Dynasty"></span><span id="__dynasty"></span><span id="__DYNASTY"></span>**\_\_Dinastia**
</dt> <dd>

Tipo di dati: **CIM \_ STRING**

Tipo di accesso: sola lettura

Nome della classe di primo livello da cui deriva la classe o l'istanza. Quando questa classe o istanza è la classe di primo livello, i valori **\_ \_ di e** **\_ \_ class** sono gli stessi.

Esempio: CIM \_ ManagedSystemElement

</dd> <dt>

<span id="__Genus"></span><span id="__genus"></span><span id="__GENUS"></span>**\_\_Genere**
</dt> <dd>

Tipo di dati: **CIM \_ SINT32**

Tipo di accesso: sola lettura

Valore utilizzato per distinguere tra classi e istanze. Questo valore è **WBEM \_ GENUS \_ CLASS** (1) per le classi e **WBEM \_ GENUS \_ INSTANCE** (2) per istanze ed eventi.

Esempio: 2

</dd> <dt>

<span id="__Namespace"></span><span id="__namespace"></span><span id="__NAMESPACE"></span>[**\_\_Namespace**](--namespace.md)
</dt> <dd>

Tipo di dati: **CIM \_ STRING**

Tipo di accesso: sola lettura

Nome dello spazio [*dei nomi*](gloss-n.md) della classe o dell'istanza.

Esempio: \\ cimv2 radice

</dd> <dt>

<span id="__Path"></span><span id="__path"></span><span id="__PATH"></span>**\_\_Percorso**
</dt> <dd>

Tipo di dati: **CIM \_ STRING**

Tipo di accesso: sola lettura

Percorso completo della classe o dell'istanza, inclusi server e spazio dei nomi.

Esempio: \\ \\ MyServer \\ root \\ cimv2:Win32 \_ OptionalFeature.Name="TelnetClient"

</dd> <dt>

<span id="__Property_Count"></span><span id="__property_count"></span><span id="__PROPERTY_COUNT"></span>**\_\_Conteggio \_ proprietà**
</dt> <dd>

Tipo di dati: **CIM \_ SINT32**

Tipo di accesso: sola lettura

Numero di proprietà non di sistema definite per la classe o l'istanza.

Esempio: 6

</dd> <dt>

<span id="__Relpath"></span><span id="__relpath"></span><span id="__RELPATH"></span>**\_\_Percorso relpath**
</dt> <dd>

Tipo di dati: **CIM \_ STRING**

Tipo di accesso: sola lettura

Percorso relativo della classe o dell'istanza.

Esempio: Win32 \_ OptionalFeature.Name="TelnetClient"

</dd> <dt>

<span id="__Server"></span><span id="__server"></span><span id="__SERVER"></span>**\_\_Server**
</dt> <dd>

Tipo di dati: **CIM \_ STRING**

Tipo di accesso: sola lettura

Nome del server che fornisce la classe o l'istanza.

Esempio: MyServer

</dd> <dt>

<span id="__Superclass"></span><span id="__superclass"></span><span id="__SUPERCLASS"></span>**\_\_Superclasse**
</dt> <dd>

Tipo di dati: **CIM \_ STRING**

Tipo di accesso: sola lettura

Nome della classe padre immediata della classe o dell'istanza.

Esempio: CIM \_ LogicalElement

</dd> </dl>

Il codice di PowerShell seguente recupera le proprietà della [**classe \_ OptionalFeature Win32,**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) che include le proprietà di sistema.


```PowerShell
Get-WmiObject win32_OptionalFeature | Where-Object {$_.name -eq "TelnetClient"}
```



L'esempio di codice precedente restituisce quanto segue:


```PowerShell
__GENUS          : 2
__CLASS          : Win32_OptionalFeature
__SUPERCLASS     : CIM_LogicalElement
__DYNASTY        : CIM_ManagedSystemElement
__RELPATH        : Win32_OptionalFeature.Name="TelnetClient"
__PROPERTY_COUNT : 6
__DERIVATION     : {CIM_LogicalElement, CIM_ManagedSystemElement}
__SERVER         : myServer
__NAMESPACE      : root\cimv2
__PATH           : \\myServer\root\cimv2:Win32_OptionalFeature.Name="TelnetClient"
Caption          : Telnet Client
Description      : 
InstallDate      : 
InstallState     : 2
Name             : TelnetClient
Status           : 
PSComputerName   : myServer
```



 

 
