---
title: Moniker di elevazione COM
description: Il moniker di elevazione COM consente alle applicazioni in esecuzione sotto controllo dell'account utente di attivare le classi COM con privilegi elevati. Per altre informazioni, vedere concentrarsi sui privilegi minimi.
ms.assetid: 1595ebb8-65af-4609-b3e7-a21209e64391
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc80774764cb99e63ed3334a8c0f9c8cedd2500
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474438"
---
# <a name="the-com-elevation-moniker"></a>Moniker di elevazione COM

Il moniker di elevazione COM consente alle applicazioni in esecuzione sotto controllo dell'account utente di attivare le classi COM con privilegi elevati. Per altre informazioni, vedere [concentrarsi sui privilegi minimi](/previous-versions/dotnet/articles/aa480194(v=msdn.10)).

## <a name="when-to-use-the-elevation-moniker"></a>Quando usare il moniker di elevazione

Il moniker di elevazione viene usato per attivare una classe COM per eseguire una funzione specifica e limitata che richiede privilegi elevati, ad esempio la modifica della data e dell'ora di sistema.

L'elevazione richiede la partecipazione sia da una classe COM che dal relativo client. La classe COM deve essere configurata in modo da supportare l'elevazione annotando la relativa voce del registro di sistema, come descritto nella sezione requisiti. Il client COM deve richiedere l'elevazione dei privilegi usando il moniker di elevazione.

Il moniker di elevazione non è progettato per garantire la compatibilità delle applicazioni. Se ad esempio si desidera eseguire un'applicazione COM legacy, ad esempio WinWord come server con privilegi elevati, è necessario configurare l'eseguibile del client COM in modo da richiedere l'elevazione, anziché attivare la classe dell'applicazione legacy con il moniker di elevazione. Quando il client COM con privilegi elevati chiama [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) usando il CLSID dell'applicazione legacy, lo stato con privilegi elevati del client viene propagato al processo server.

Non tutte le funzionalità COM sono compatibili con l'elevazione. Le funzionalità che non funzioneranno includono:

-   L'elevazione dei privilegi non viene propagata da un client a un server COM remoto. Se un client attiva un server COM remoto con il moniker di elevazione, il server non verrà elevato, anche se supporta l'elevazione dei privilegi.
-   Se una classe COM con privilegi elevati utilizza la rappresentazione durante una chiamata COM, potrebbe perdere i privilegi elevati durante la rappresentazione.
-   Se un server COM con privilegi elevati registra una classe nella tabella degli oggetti in esecuzione (ROT), la classe non sarà disponibile per i client non con privilegi elevati.
-   Un processo con privilegi elevati tramite il meccanismo UAC non carica le classi per utente durante le attivazioni COM. Per le applicazioni COM, ciò significa che le classi COM dell'applicazione devono essere installate nell'hive del registro di sistema del **\_ \_ computer locale HKEY** se l'applicazione deve essere usata sia da account senza privilegi che da account con privilegi. Le classi COM dell'applicazione devono essere installate solo nell'hive **\_ utenti HKEY** se l'applicazione non viene mai usata da account con privilegi.
-   Il trascinamento della selezione non è consentito da applicazioni non elevate ad elevate.

## <a name="requirements"></a>Requisiti

Per usare il moniker di elevazione per attivare una classe COM, è necessario che la classe sia configurata per l'esecuzione come utente di avvio o come identità dell'applicazione "Activate As Activator". Se la classe è configurata in modo da essere eseguita con qualsiasi altra identità, l'attivazione restituisce il valore di errore della coordinata di CO \_ E \_ \_ \_ deve \_ essere \_ AAA.

La classe deve anche essere annotata con un nome visualizzato "descrittivo" che è compatibile con l'interfaccia utente multilingue (MUI). Questa operazione richiede la seguente voce del registro di sistema:

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      LocalizedString = displayName
```

Se questa voce non è presente, l'attivazione restituisce la CO \_ E l'errore \_ \_ DisplayName mancante. Se il file MUI non è presente, viene restituito il codice di errore della funzione [**RegLoadMUIStringW**](/windows/desktop/api/winreg/nf-winreg-regloadmuistringa) .

Facoltativamente, per specificare un'icona dell'applicazione che deve essere visualizzata dall'interfaccia utente del controllo dell'account utente, aggiungere la chiave del registro di sistema seguente:

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      Elevation
         IconReference = applicationIcon
```

**IconReference** usa lo stesso formato di **LocalizedString**:

@*pathtobinary*,*-numerorisorsa*

Inoltre, è necessario che il componente COM sia firmato per visualizzare l'icona.

La classe COM deve essere annotata anche come abilitata per LUA. Questa operazione richiede la seguente voce del registro di sistema:

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      Elevation
         Enabled = 1
```

Se questa voce non è presente, l'attivazione restituisce l'elevazione della CO E dell'errore \_ \_ \_ disabilitata.

Si noti che queste voci devono esistere nell' \_ hive del \_ computer locale hKey, non l' \_ utente corrente di HKEY o l' \_ \_ hive degli utenti HKEY. In questo modo si impedisce agli utenti di elevare le classi COM che non dispongono anche dei privilegi per la registrazione.

## <a name="the-elevation-moniker-and-the-elevation-ui"></a>Il moniker di elevazione e l'interfaccia utente di elevazione

Se il client è già elevato, l'utilizzo del moniker di elevazione non comporterà la visualizzazione dell'interfaccia utente di elevazione.

## <a name="how-to-use-the-elevation-moniker"></a>Come usare il moniker di elevazione

Il moniker di elevazione è un moniker COM standard, simile ai moniker della sessione, della partizione o della coda. Indirizza una richiesta di attivazione a un server specificato con il livello di elevazione specificato. Il CLSID da attivare viene visualizzato nella stringa del moniker.

Il moniker di elevazione dei privilegi supporta i token del livello di esecuzione seguenti:

1.  Amministratore
2.  Più alta

La sintassi è la seguente:

``` syntax
Elevation:Administrator!new:{guid}
Elevation:Highest!new:{guid}
```

La sintassi precedente usa il moniker "New" per restituire un'istanza della classe COM specificata da *GUID*. Si noti che il moniker "New" usa internamente l'interfaccia [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) per ottenere un oggetto classe e quindi chiama [**IClassFactory:: CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) .

Il moniker di elevazione può essere usato anche per ottenere un oggetto classe, che implementa [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory). Il chiamante chiama quindi [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) per ottenere un'istanza dell'oggetto. La sintassi è la seguente:

``` syntax
Elevation:Administrator!clsid:{guid}
```

## <a name="sample-code"></a>Codice di esempio

Nell'esempio di codice riportato di seguito viene illustrato come utilizzare il moniker di elevazione. Si presuppone che sia già stato inizializzato COM sul thread corrente.


```C++
HRESULT CoCreateInstanceAsAdmin(HWND hwnd, REFCLSID rclsid, REFIID riid, __out void ** ppv)
{
    BIND_OPTS3 bo;
    WCHAR  wszCLSID[50];
    WCHAR  wszMonikerName[300];

    StringFromGUID2(rclsid, wszCLSID, sizeof(wszCLSID)/sizeof(wszCLSID[0])); 
    HRESULT hr = StringCchPrintf(wszMonikerName, sizeof(wszMonikerName)/sizeof(wszMonikerName[0]), L"Elevation:Administrator!new:%s", wszCLSID);
    if (FAILED(hr))
        return hr;
    memset(&bo, 0, sizeof(bo));
    bo.cbStruct = sizeof(bo);
    bo.hwnd = hwnd;
    bo.dwClassContext  = CLSCTX_LOCAL_SERVER;
    return CoGetObject(wszMonikerName, &bo, riid, ppv);
}
```



Esegui [**binding \_ OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) è una novità di Windows Vista. Viene derivato da [**binding \_ OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1).

L'unica aggiunta è un campo **HWND** , **HWND**. Questo handle rappresenta una finestra che diventa il proprietario dell'interfaccia utente dell'elevazione dei privilegi, se applicabile.

Se **HWND** è **null**, com chiamerà [GetActiveWindow](/windows/win32/api/winuser/nf-winuser-getactivewindow) per trovare un handle di finestra associato al thread corrente. Questo caso può verificarsi se il client è uno script, che non può compilare una [**struttura \_ OPTS3 di binding**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) . In questo caso, COM tenterà di utilizzare la finestra associata al thread di script.

## <a name="over-the-shoulder-ots-elevation"></a>Innalzamento di livello (OTS)

L'elevazione dei privilegi (OTS) si riferisce allo scenario in cui un client esegue un server COM con le credenziali di un amministratore anziché la propria. Il termine "over the Shoulder" indica che l'amministratore sta controllando la spalla del client mentre il client esegue il server.

Questo scenario può causare un problema per le chiamate COM al server, perché il server potrebbe non chiamare [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) in modo esplicito (ovvero a livello di codice) o in modo implicito (ovvero, in modo dichiarativo, usando il registro di sistema). Per tali server, COM calcola un descrittore di sicurezza che consente solo agli amministratori autonomi, di sistema e predefiniti \\ di effettuare chiamate com al server. Questa disposizione non funzionerà negli scenari OTS. Il server deve invece chiamare **CoInitializeSecurity**, in modo esplicito o implicito, e specificare un ACL che includa il SID del gruppo interattivo e il sistema.

Nell'esempio di codice seguente viene illustrato come creare un descrittore di sicurezza (SD) con il SID del gruppo interattivo.

``` syntax
BOOL GetAccessPermissionsForLUAServer(SECURITY_DESCRIPTOR **ppSD)
{
// Local call permissions to IU, SY
    LPWSTR lpszSDDL = L"O:BAG:BAD:(A;;0x3;;;IU)(A;;0x3;;;SY)";
    SECURITY_DESCRIPTOR *pSD;
    *ppSD = NULL;

    if (ConvertStringSecurityDescriptorToSecurityDescriptorW(lpszSDDL, SDDL_REVISION_1, (PSECURITY_DESCRIPTOR *)&pSD, NULL))
    {
        *ppSD = pSD;
        return TRUE;
    }

    return FALSE;
}
```

Nell'esempio di codice seguente viene illustrato come chiamare in modo implicito [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) con la SD dall'esempio di codice precedente:


```C++
// hKey is the HKCR\AppID\{GUID} key
BOOL SetAccessPermissions(HKEY hkey, PSECURITY_DESCRIPTOR pSD)
{
    BOOL bResult = FALSE;
    DWORD dwLen = GetSecurityDescriptorLength(pSD);
    LONG lResult;
    lResult = RegSetValueExA(hkey, 
        "AccessPermission",
        0,
        REG_BINARY,
        (BYTE*)pSD,
        dwLen);
    if (lResult != ERROR_SUCCESS) goto done;
    bResult = TRUE;
done:
    return bResult;
}
```



Nell'esempio di codice seguente viene illustrato come chiamare in modo esplicito [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) con la SD precedente:


```C++
// Absolute SD values
PSECURITY_DESCRIPTOR pAbsSD = NULL;
DWORD AbsSdSize = 0;
PACL  pAbsAcl = NULL;
DWORD AbsAclSize = 0;
PACL  pAbsSacl = NULL;
DWORD AbsSaclSize = 0;
PSID  pAbsOwner = NULL;
DWORD AbsOwnerSize = 0;
PSID  pAbsGroup = NULL;
DWORD AbsGroupSize = 0;

MakeAbsoluteSD (
    pSD,
    pAbsSD,
    &AbsSdSize,
    pAbsAcl,
    &AbsAclSize,
    pAbsSacl,
    &AbsSaclSize,
    pAbsOwner,
    &AbsOwnerSize,
    pAbsGroup,
    &AbsGroupSize
);

if (ERROR_INSUFFICIENT_BUFFER == GetLastError())
{
    pAbsSD = (PSECURITY_DESCRIPTOR)LocalAlloc(LMEM_FIXED, AbsSdSize);
    pAbsAcl = (PACL)LocalAlloc(LMEM_FIXED, AbsAclSize);
    pAbsSacl = (PACL)LocalAlloc(LMEM_FIXED, AbsSaclSize);
    pAbsOwner = (PSID)LocalAlloc(LMEM_FIXED, AbsOwnerSize);
    pAbsGroup = (PSID)LocalAlloc(LMEM_FIXED, AbsGroupSize);

    if ( ! (pAbsSD && pAbsAcl && pAbsSacl && pAbsOwner && pAbsGroup))
    {
        hr = E_OUTOFMEMORY;
        goto Cleanup;
    }
    if ( ! MakeAbsoluteSD(
        pSD,
        pAbsSD,
        &AbsSdSize,
        pAbsAcl,
        &AbsAclSize,
        pAbsSacl,
        &AbsSaclSize,
        pAbsOwner,
        &AbsOwnerSize,
        pAbsGroup,
        &AbsGroupSize
        ))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        goto Cleanup;
    }
}
else
{
    hr = HRESULT_FROM_WIN32(GetLastError());
    goto Cleanup;
}

// Call CoinitilizeSecurity.
```



## <a name="com-permissions-and-mandatory-access-labels"></a>Autorizzazioni COM e etichette di accesso obbligatorie

Windows Vista introduce la nozione di *etichette di accesso obbligatorie* nei descrittori di sicurezza. L'etichetta determina se i client possono ottenere l'accesso in esecuzione a un oggetto COM. L'etichetta viene specificata nella parte dell'elenco di controllo di accesso di sistema (SACL) del descrittore di sicurezza. In Windows Vista, COM supporta l' \_ etichetta obbligatoria di sistema \_ \_ senza eseguire l' \_ \_ etichetta. I SACL nelle autorizzazioni COM vengono ignorati nei sistemi operativi precedenti a Windows Vista.

A partire da Windows Vista, dcomcnfg.exe non supporta la modifica del livello di integrità (IL) nelle autorizzazioni COM. Deve essere impostato a livello di codice.

Nell'esempio di codice seguente viene illustrato come creare un descrittore di sicurezza COM con un'etichetta che consente le richieste di avvio/attivazione da tutti i client IL basso. Si noti che le etichette sono valide per le autorizzazioni di avvio/attivazione e di chiamata. Pertanto, è possibile scrivere un server COM che non consente l'avvio, l'attivazione o le chiamate da client con un determinato IL. Per ulteriori informazioni sui livelli di integrità, vedere la sezione "informazioni sul meccanismo di integrità di Windows Vista" per [comprendere e utilizzare la modalità protetta di Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/).


```C++
BOOL GetLaunchActPermissionsWithIL (SECURITY_DESCRIPTOR **ppSD)
{
// Allow World Local Launch/Activation permissions. Label the SD for LOW IL Execute UP
    LPWSTR lpszSDDL = L"O:BAG:BAD:(A;;0xb;;;WD)S:(ML;;NX;;;LW)";
    if (ConvertStringSecurityDescriptorToSecurityDescriptorW(lpszSDDL, SDDL_REVISION_1, (PSECURITY_DESCRIPTOR *)&pSD, NULL))
    {
        *ppSD = pSD;
        return TRUE;
    }
}

BOOL SetLaunchActPermissions(HKEY hkey, PSECURITY_DESCRIPTOR pSD)
{
    
    BOOL bResult = FALSE;
    DWORD dwLen = GetSecurityDescriptorLength(pSD);
    LONG lResult;
    lResult = RegSetValueExA(hkey, 
        "LaunchPermission",
        0,
        REG_BINARY,
        (BYTE*)pSD,
        dwLen);
    if (lResult != ERROR_SUCCESS) goto done;
    bResult = TRUE;
done:
    return bResult;
};
```



## <a name="cocreateinstance-and-integrity-levels"></a>CoCreateInstance e livelli di integrità

Per impostazione predefinita, il comportamento di [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) è stato modificato in Windows Vista, per impedire che i client il ridotti il binding ai server com. Il server deve consentire esplicitamente tali associazioni specificando il SACL. Le modifiche a **CoCreateInstance** sono le seguenti:

1.  Quando si avvia un processo server COM, il il nel token del processo server viene impostato sul client o sul token del server il, a seconda del valore minore.
2.  Per impostazione predefinita, COM impedisce ai client di basso livello di eseguire IL binding alle istanze in esecuzione di qualsiasi server COM. Per consentire l'associazione, il descrittore di sicurezza di avvio/attivazione di un server COM deve contenere un SACL che specifica l'etichetta IL bassa (vedere la sezione precedente per il codice di esempio per creare un descrittore di sicurezza di questo tipo).

## <a name="elevated-servers-and-rot-registrations"></a>Server con privilegi elevati e registrazioni ROT

Se un server COM vuole registrarsi nella tabella degli oggetti in esecuzione (ROT) e consentire a qualsiasi client di accedere alla registrazione, è necessario usare il \_ flag ROTFLAGS ALLOWANYCLIENT. Un server COM "Activate As Activator" non è in grado di specificare ROTFLAGS \_ ALLOWANYCLIENT perché la gestione controllo servizi DCOM (Dcomscm) impone un controllo di spoofing rispetto a questo flag. Pertanto, in Windows Vista, COM aggiunge il supporto per una nuova voce del registro di sistema che consente al server di stabilire che le registrazioni ROT saranno rese disponibili per qualsiasi client:

```
HKEY_LOCAL_MACHINE\Software\Classes\AppID
   {APPID}
      ROTFlags
```

L'unico valore valido per questa \_ voce reg DWORD è:

``` syntax
ROTREGFLAGS_ALLOWANYCLIENT 0x1
```

La voce deve esistere nell'hive **del \_ \_ computer locale HKEY** .

Questa voce fornisce un server "Activate As Activator" con la stessa funzionalità fornita da ROTFLAGS \_ ALLOWANYCLIENT per un server RunAs.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> <dt>

[Understanding and Working in Protected Mode Internet Explorer (Informazioni e utilizzo della modalità protetta di Internet Explorer)](/previous-versions/windows/internet-explorer/ie-developer/)
</dt> </dl>

 

 