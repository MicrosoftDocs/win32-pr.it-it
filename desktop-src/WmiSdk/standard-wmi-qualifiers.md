---
description: Di seguito sono elencati i qualificatori standard specifici di WMI.
ms.assetid: 63bdbafc-51f3-4714-8b7e-9d5a61cef45e
ms.tgt_platform: multiple
title: Qualificatori WMI standard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Standard
api_type:
- NA
api_location: ''
ms.openlocfilehash: e73b053354d86c4a56698a7a65c17e302425f56d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314574"
---
# <a name="standard-wmi-qualifiers"></a>Qualificatori WMI standard

Di seguito sono elencati i qualificatori standard specifici di WMI.

<dt>

<span id="Amendment"></span><span id="amendment"></span><span id="AMENDMENT"></span>**Emendamento**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: classi

Indica che una classe contiene qualificatori modificati localizzati. Il valore predefinito è **true**.

La classe associata può essere convertita. Per accedere alla versione tradotta, utilizzare l'identificatore delle impostazioni locali per costruire un nome di spazio dei nomi.

</dd> <dt>

<span id="Bypass_GetObject"></span><span id="bypass_getobject"></span><span id="BYPASS_GETOBJECT"></span>**Bypass \_ GetObject**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: metodi

Indica che la chiamata al metodo deve passare direttamente alla chiamata **ExecMethodAsync** del provider anziché al provider che effettua prima una chiamata a **GetObject** per convalidare il percorso dell'oggetto. Il valore predefinito è **false**. L'uso di **bypass \_ GetObject** può migliorare significativamente le prestazioni.

Prima di usare il comando **bypass \_ GetObject**, assicurarsi che non vengano eseguite nessuna delle azioni seguenti:

-   Derivare una classe dalla classe.
-   Eseguire l'override del metodo con il qualificatore **\_ GetObject di bypass** .

L'impossibilità di seguire queste precauzioni può comportare la chiamata all'implementazione del metodo della classe padre anziché della classe figlio. Per ulteriori informazioni, vedere Utilizzo del \_ qualificatore GetObject di bypass.

</dd> <dt>

<span id="CIM_Key"></span><span id="cim_key"></span><span id="CIM_KEY"></span>**\_Chiave CIM**
</dt> <dd>

Tipo di dati **: \_ booleano CIM**

Si applica a: Proprietà

Indica che la proprietà associata è una proprietà chiave in CIM ma non in WMI.

</dd> <dt>

<span id="CIMType"></span><span id="cimtype"></span><span id="CIMTYPE"></span>[**CIMType**](cimtype-qualifier.md)
</dt> <dd>

Tipo di dati: **VT \_ BSTR**

Si applica a: proprietà, metodi, parametri

Contiene testo che descrive il tipo di una proprietà.

</dd> <dt>

<span id="ClassContext"></span><span id="classcontext"></span><span id="CLASSCONTEXT"></span>**ClassContext**
</dt> <dd>

Tipo di dati: **VT \_ BSTR**

Si applica a: classi

Indica che una classe dispone di istanze associate a più informazioni in modo dinamico fornite da un provider.

</dd> <dt>

<span id="Deprecated"></span><span id="deprecated"></span><span id="DEPRECATED"></span>**Deprecato**
</dt> <dd>

Tipo di dati **: \_ booleano CIM**

Si applica a: proprietà, classi

Indica che la proprietà è stata sostituita da un'altra proprietà.

</dd> <dt>

<span id="Display"></span><span id="display"></span><span id="DISPLAY"></span>**Visualizzare**
</dt> <dd>

Si applica a: classi, proprietà

**UUID** della classe associata.

</dd> <dt>

<span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>[**Dinamico**](dynamic-qualifier.md)
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: classi, proprietà

Indica una classe le cui istanze vengono create dinamicamente. Il valore di questo qualificatore deve essere impostato su **true**.

</dd> <dt>

<span id="DynProps"></span><span id="dynprops"></span><span id="DYNPROPS"></span>**DynProps**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: classi, istanze

Indica che un'istanza contiene valori forniti dai provider di proprietà dinamici. Il valore predefinito è **true**.

È necessario specificare questo qualificatore in tale istanza. È consentito solo il valore **true** .

</dd> <dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>**Fissa**
</dt> <dd>

Tipo di dati **: \_ booleano CIM**

Si applica a: istanze di

Indica che il valore di questa proprietà non può essere modificato nel corso della durata dell'istanza.

</dd> <dt>

<span id="ID"></span><span id="id"></span>**ID**
</dt> <dd>

Tipo di dati: **VT \_ I4**

Si applica a: proprietà, parametri

Identifica in modo univoco e Sequenzia una proprietà o un parametro di metodo quando le istruzioni MOF vengono generate automaticamente.

Questo qualificatore è necessario solo per i parametri del metodo. Quando si creano parametri per un metodo, i progettisti di classi devono iniziare con ID (0) per il primo parametro e usare ogni numero intero successivo per ogni parametro successivo. Se i qualificatori **ID** vengono omessi intenzionalmente, il compilatore MOF genera automaticamente i qualificatori **ID** .

</dd> <dt>

<span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Implementato**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: metodi

Indica che un metodo dispone di un'implementazione fornita da un provider.

</dd> <dt>

<span id="InstanceContext"></span><span id="instancecontext"></span><span id="INSTANCECONTEXT"></span>**InstanceContext**
</dt> <dd>

Tipo di dati: **VT \_ BSTR**

Si applica a: istanze di

Indica che un'istanza contiene valori forniti da un provider di proprietà dinamico.

Il valore viene passato al provider di proprietà come argomento al metodo [**IWbemPropertyProvider:: GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) .

</dd> <dt>

<span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Locale**
</dt> <dd>

Tipo di dati: **VT \_ BSTR**

Si applica a: classi o istanze

Specifica la lingua dell'origine per una classe o un'istanza. Per altre informazioni sui valori delle impostazioni locali, vedere [codici delle impostazioni locali](#locale-codes).

</dd> <dt>

<span id="NamespaceSecuritySDDL"></span><span id="namespacesecuritysddl"></span><span id="NAMESPACESECURITYSDDL"></span>**NamespaceSecuritySDDL**
</dt> <dd>

Tipo di dati: **matrice di stringhe**

Si applica a: istanze dello spazio dei nomi

Specifica un descrittore di sicurezza per lo spazio dei nomi in formato [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language) . Per ulteriori informazioni, vedere [impostazione della sicurezza dello spazio dei nomi quando viene creato lo spazio dei nomi](setting-namespace-security-when-the-namespace-is-created.md). La stringa SDDL viene elaborata da WMI per stabilire la sicurezza dello spazio dei nomi ma non memorizzata come stringa. Se non viene specificato alcun descrittore di sicurezza, viene utilizzata la sicurezza predefinita. Per altre informazioni, vedere [impostazione dei descrittori di sicurezza spazio dei nomi](setting-namespace-security-descriptors.md).

</dd> <dt>

<span id="Optional"></span><span id="optional"></span><span id="OPTIONAL"></span>**Opzionale**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: parametri

Indica che un parametro non è obbligatorio e che dispone di un valore predefinito corretto.

</dd> <dt>

<span id="Privileges"></span><span id="privileges"></span><span id="PRIVILEGES"></span>**Privilegi**
</dt> <dd>

Tipo di dati: **matrice di stringhe**

Si applica a: proprietà, metodi

Insieme di valori utilizzati per informare il client quali privilegi sono necessari per creare istanze, compilare proprietà o eseguire metodi. Il valore predefinito è **false**.

</dd> <dt>

<span id="PropertyContext"></span><span id="propertycontext"></span><span id="PROPERTYCONTEXT"></span>**PropertyContext**
</dt> <dd>

Tipo di dati: **VT \_ BSTR**

Si applica a: Proprietà

Indica che una proprietà dell'istanza contiene valori forniti dai provider di proprietà dinamici.

È necessario specificare questo qualificatore su una proprietà di questo tipo. Il valore viene passato al provider di proprietà come argomento di [**IWbemPropertyProvider:: GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty).

</dd> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Provider**
</dt> <dd>

Tipo di dati: **VT \_ BSTR**

Si applica a: classi

Il valore di questo qualificatore è il nome del provider dinamico che fornisce istanze della classe e aggiorna i dati dell'istanza. Questo nome deve essere registrato con WMI creando un'istanza della classe [**\_ \_ Win32Provider**](--win32provider.md) con la proprietà **Name** che contiene questo nome. Quando questo qualificatore viene specificato in una classe le cui istanze vengono fornite in modo dinamico, è necessario specificare anche il qualificatore **dinamico** .

</dd> <dt>

<span id="RequiresEncryption"></span><span id="requiresencryption"></span><span id="REQUIRESENCRYPTION"></span>**RequiresEncryption**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: istanze dello spazio dei nomi

Se è impostato su **true**, **RequiresEncryption** contrassegna uno spazio dei nomi in modo che le applicazioni e gli script client debbano connettersi con l'autenticazione crittografata. Il livello di autenticazione deve essere impostato **su \_ \_ \_ \_ PKT \_ privacy a livello** di autenticazione di RPC C in C++. Nel Visual Basic di scripting, il livello di autenticazione deve essere impostato su **WbemAuthenticationLevelPktPrivacy**. Per altre informazioni, vedere [impostazione dei descrittori di sicurezza spazio dei nomi](setting-namespace-security-descriptors.md). Il qualificatore viene usato in [*MOF*](gloss-m.md) con il comando del preprocessore dello spazio dei nomi pragma.

Per altre informazioni, vedere [impostazione del livello di sicurezza del processo predefinito con C++](setting-the-default-process-security-level-using-c-.md) o [impostazione del livello di sicurezza del processo predefinito tramite VBScript](setting-the-default-process-security-level-using-vbscript.md). I livelli di autenticazione di scripting sono definiti in [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).

</dd> <dt>

<span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Singleton**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: classi

Definisce una classe che può avere una sola istanza e che non contiene proprietà chiave.

È consentito solo il valore **true** (impostazione predefinita).

</dd> <dt>

<span id="Static"></span><span id="static"></span><span id="STATIC"></span>**Statico**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: metodi

Indica se un metodo può essere chiamato utilizzando la definizione della classe o le relative istanze.

Il metodo non può essere richiamato da un'istanza di.

</dd> <dt>

<span id="SubType"></span><span id="subtype"></span><span id="SUBTYPE"></span>**Sottotipo**
</dt> <dd>

Tipo di dati: **VT \_ BSTR**

Si applica a: Proprietà

Indica che una proprietà di tipo **CIM \_ DateTime** rappresenta un intervallo di tempo anziché un'ora specifica.

Per identificare la proprietà come intervallo, il valore di questo qualificatore deve essere "Interval". Tutti gli altri valori per questo qualificatore sono riservati per un uso futuro.

</dd> <dt>

<span id="UUID"></span><span id="uuid"></span>**UUID**
</dt> <dd>

Tipo di dati: **String**

Si applica a: classi

Identificatore univoco universale applicato alla classe.

</dd> <dt>

<span id="ClassVersion"></span><span id="classversion"></span><span id="CLASSVERSION"></span>**ClassVersion**
</dt> <dd>

Tipo di dati: **String**

Si applica a: classi

Numero di versione dell'oggetto classe. Il valore predefinito è **null**. Il numero di versione viene incrementato quando vengono apportate modifiche alla classe.

</dd> <dt>

<span id="WritePrivileges"></span><span id="writeprivileges"></span><span id="WRITEPRIVILEGES"></span>**WritePrivileges**
</dt> <dd>

Tipo di dati: **matrice di stringhe**

Si applica a: Proprietà

Set di valori che indica quali privilegi di sistema devono essere disponibili e abilitati per un'operazione di scrittura corretta.

</dd> </dl>

## <a name="remarks"></a>Commenti

### <a name="locale-codes"></a>Codici delle impostazioni locali

Il formato di un codice delle impostazioni locali è "MS \_ <Three Digit Language ID> ". Ad esempio, le impostazioni locali inglesi sono MS \_ 409. Nella tabella seguente sono elencati gli ID della lingua.



| Linguaggio              | ID lingua (esadecimale) |
|-----------------------|---------------------------|
| Arabo                | 401                       |
| Portoghese (Brasile)   | 416                       |
| Cinese (semplificato)  | 804                       |
| Cinese (tradizionale) | 404                       |
| Ceco                 | 405                       |
| Danese                | 406                       |
| Olandese                 | 413                       |
| Inglese (predefinito)     | 409                       |
| Finlandese               | 40B                       |
| Francese                | 40C                       |
| Tedesco                | 407                       |
| Greco                 | 408                       |
| Ebraico                | 40D                       |
| Ungherese             | 40E                       |
| Italiano               | 410                       |
| Giapponese              | 411                       |
| Coreano                | 412                       |
| Norvegese             | 414                       |
| Polacco                | 415                       |
| Portoghese (Portogallo) | 816                       |
| Russo               | 419                       |
| Spagnolo               | c0a                       |
| Svedese               | 41 quinquies                       |
| Turco               | 41F                       |



 

### <a name="using-the-bypass_getobject-qualifier"></a>Uso del \_ qualificatore GetObject di bypass

L'uso del qualificatore **\_ GetObject di bypass** su un metodo può produrre risultati confusi.

Nell'esempio seguente vengono definite le classi **Shape** e **Circle** . Si noti che la classe **Circle** è derivata dalla classe **Shape** .


```VB
class Shape
{
   string Name;
   uint32 DrawIt();  // - draws an irregular geometric shape
};

class Circle : Shape
{
   uint32 DrawIt();  // - draws a circle
};
```



La chiamata seguente a **ExecMethod** usa un oggetto **Circle** denominato "tocircle" per creare un cerchio.


```VB
ExecMethod("Shape.Name='MyCircle'","DrawIt");
```



Nello scenario precedente, WMI chiama **GetObject**; rileva che "Shape. Name =' il cerchio '" è un **cerchio**; ed esegue l'implementazione **Circle** di **drawit**. Tuttavia, se si usa il qualificatore **\_ GetObject di bypass** in **drawit**, WMI non chiama **GetObject**, non rileva che "Shape. Name =' il cerchio '" è un **cerchio** ed esegue l'implementazione della **forma** di **drawit** invece dell'implementazione del **cerchio** di **drawit**.

La chiamata seguente a **ExecMethod** richiama sempre l'implementazione corretta di **drawit**.


```VB
ExecMethod("Circle.Name='MyCircle'","DrawIt");
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Impostazione di descrittori di sicurezza spazio dei nomi](setting-namespace-security-descriptors.md)
</dt> <dt>

[Qualificatori WMI](wmi-qualifiers.md)
</dt> <dt>

[Aggiunta di un qualificatore](adding-a-qualifier.md)
</dt> </dl>

 

