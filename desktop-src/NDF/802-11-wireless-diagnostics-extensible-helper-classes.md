---
title: 802.11 Wireless Diagnostics Extensible Helper Classes
description: L'infrastruttura di diagnostica wireless predefinita ha due punti di estensione. Classe helper padrePurposeRevised Native Wifi (RNWF) Extensible Helper ClassDiagnoses issues related to 802.11 connectivity extensions (Classe helper estendibile RNWF)Diagnostica i problemi relativi alle estensioni di connettività 802.11.
ms.assetid: b54f836d-4fae-4e71-bf7b-af5a6e9e615c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3b7ac72cb42b12a96e5c57db0897a13d49d76370126e119ac2f5ed457d55c9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133446"
---
# <a name="80211-wireless-diagnostics-extensible-helper-classes"></a>802.11 Wireless Diagnostics Extensible Helper Classes

L'infrastruttura di diagnostica wireless predefinita ha due punti di estensione.

| Classe helper padre                                | Scopo                                                           |
|----------------------------------------------------|-------------------------------------------------------------------|
| Classe helper estendibile RNWF (Native Wifi) modificata | Diagnostica i problemi relativi alle estensioni di connettività 802.11.       |
| Classe helper L2Security Extensible                 | Diagnostica i problemi relativi alle estensioni del protocollo di sicurezza di livello 2. |



 

> [!Note]  
> Una classe helper di terze parti deve eseguire la registrazione con entrambe le classi helper padre per garantire che venga chiamata la classe di terze parti. Per altre informazioni sulla registrazione, vedere [Registrazione delle estensioni della classe helper NDF.](registering-ndf-helper-class-extensions.md)

 

## <a name="rnwf-extensible-helper-class"></a>Classe helper Estendibile RNWF

Nome della classe helper padre

``` syntax
Parent = L"RNWF Extensible Helper Class";
```

La classe helper estendibile RNWF (Native Wifi) modificata è l'elemento padre per le classi helper di terze parti che diagnosticano i problemi correlati all'estensione dei protocolli 802.11 usati dal Wi-Fi nativo.

I due attributi chiave forniti dalla classe helper RNWF sono il GUID dell'interfaccia in cui si è verificato il problema e il contesto di connessione.

-   GUID interfaccia: questo attributo è denominato "ID interfaccia" ed è di tipo **AT \_ GUID**.

-   Contesto di connessione: questo attributo è denominato ID di rete ed è di tipo AT \_ OCTET \_ STRING. Questa stringa è in realtà un buffer della struttura \_ WHV WLAN ID definita \_ in \_ Wlanihv.h. Questa struttura è definita come segue.

    ``` syntax
#define WDIAG_IHV_WLAN_ID_FLAG_SECURITY_ENABLED               0x00000001
    typedef
    struct _WDIAG_IHV_WLAN_ID
    {
        WCHAR                        strProfileName [MS_MAX_PROFILE_NAME_LENGTH];
        DOT11_SSID                   Ssid;
        DOT11_BSS_TYPE               BssType;
        DWORD                        dwFlags;           // Flags defined above
        DWORD                        dwReasonCode;      // Set only when an applicable reason code is available
    }
    WDIAG_IHV_WLAN_ID, *PWDIAG_IHV_WLAN_ID;
    ```

> [!Note]  
> **WDIAG \_ IHV \_ WLAN \_ ID FLAG \_ SECURITY \_ \_ ENABLED** è l'unico **valore dwFlags** possibile.

 

L'attributo corrispondente per la classe helper di terze parti deve essere uguale all'ID servizio del modulo software corrispondente. Questo è anche lo stesso nome che la terza parte deve essere registrata nel Registro di sistema. La diagnostica wireless eseguirà una query sull'ID servizio durante la sessione wireless in cui si è verificato il problema. Le informazioni verranno restituite a NDF, che determinerà se la classe helper di terze parti è presente e registrata e quindi la chiamerà.

Nella tabella seguente sono elencati gli attributi corrispondenti per la classe helper estendibile RNWF.



| Nome          | Type    | valore                         |
|---------------|---------|-------------------------------|
| DIAGNOSTICSID | REG \_ SZ | \[Stringa GUID DiagnosticsID \_ \_ |



 

## <a name="l2security-extensible-helper-class"></a>Classe helper L2Security Extensible

Nome della classe helper padre

``` syntax
Parent = L"Extensible L2Sec Helper Class";
```

La classe helper estendibile Layer 2 Security (L2Security) è l'elemento padre per le classi helper di terze parti che diagnosticano i problemi correlati ai servizi e ai moduli software corrispondenti che sostituiscono la funzionalità di sicurezza di livello 2.

I due attributi chiave forniti dalla classe helper di sicurezza di livello 2 sono il GUID dell'interfaccia in cui si è verificato il problema e il contesto di connessione.

-   GUID interfaccia: questo attributo è denominato "ID interfaccia" ed è di tipo **AT \_ GUID**.

-   Contesto di connessione: questo attributo è denominato ID di rete ed è di tipo AT \_ OCTET \_ STRING. Questa stringa è in realtà un buffer della struttura \_ WHV WLAN ID definita \_ in \_ wlanihv.h. Questa struttura è definita come segue.

    ``` syntax
#define WDIAG_IHV_WLAN_ID_FLAG_SECURITY_ENABLED               0x00000001
    typedef
    struct _WDIAG_IHV_WLAN_ID
    {
        WCHAR                        strProfileName [MS_MAX_PROFILE_NAME_LENGTH];
        DOT11_SSID                   Ssid;
        DOT11_BSS_TYPE               BssType;
        DWORD                        dwFlags;           // Flags defined above
        DWORD                        dwReasonCode;      // Set only when an applicable reason code is available
    }
    WDIAG_IHV_WLAN_ID, *PWDIAG_IHV_WLAN_ID;
    ```

> [!Note]  
> **WDIAG \_ IHV \_ WLAN \_ ID FLAG \_ SECURITY \_ \_ ENABLED** è l'unico **valore dwFlags** possibile.

 

L'attributo corrispondente per la classe helper di terze parti deve essere uguale all'ID servizio del modulo software corrispondente. Questo è anche lo stesso nome che la terza parte deve essere registrata nel Registro di sistema. La diagnostica wireless eseguirà una query sull'ID servizio durante la sessione wireless in cui si è verificato il problema. Le informazioni verranno restituite a NDF, che determinerà se la classe helper di terze parti è presente e registrata e quindi la chiamerà.

Nella tabella seguente sono elencati gli attributi corrispondenti per la classe helper estendibile Layer 2 Security.



| Nome          | Type    | valore                         |
|---------------|---------|-------------------------------|
| DIAGNOSTICSID | REG \_ SZ | \[Stringa GUID DiagnosticsID \_ \_ |



 

## <a name="matching-attributes"></a>Attributi corrispondenti

**DIAGNOSTICSID**

802.11 Diagnostica wireless eseguirà una query su *DiagnosticsID* dal servizio Wi-Fi nativo di base per verificare se eventuali estensioni wireless di terze parti o moduli di sicurezza sono installati e coinvolti nella connessione. Diagnostica wireless fornirà quindi ipotesi a queste classi helper di terze parti usando *DiagnosticsID* come attributo corrispondente. Tutte le classi helper di terze parti devono essere incluse in e installate con il pacchetto driver associato. DiagnosticsID *verrà* definito nel file INF del miniport come chiave del Registro di sistema nella [direttiva AddReg.](https://msdn.microsoft.com/library/ms794514.aspx)

``` syntax
HKR,Ndi\IHVExtensions, DiagnosticsID,0, "<Diagnostics ID GUID>"
```

Questa chiave definisce l'ID della classe helper wireless per il modulo software di terze parti. Questa chiave è facoltativa per il framework di estendibilità, ma è necessaria se l'implementazione include una classe helper wireless IHV che si collega alla funzione NDF e può diagnosticare i problemi di connettività correlati alle estensioni wireless o di sicurezza RNWF. Le classi helper di diagnostica WLAN MS eseguiranno una query su questo ID dal Servizio configurazione automatica wireless quando vengono installati i moduli IHV e fornirà questo ID come attributo di riferimento o corrispondente a NDF durante una sessione di diagnostica in modo che NDF possa chiamare la classe helper wireless di terze parti appropriata quando necessario.

**\[Stringa GUID DiagnosticsID \_ \_\]**

Questo valore deve essere una stringa di tutte le lettere maiuscole. Ad esempio, "{12345678-9ABC-DEF0-1234-56789ABCDEF0}".

## <a name="scope-of-80211-wireless-diagnostics-helper-classes"></a>Ambito delle classi helper di diagnostica wireless 802.11

Le classi helper di diagnostica wireless 802.11 attualmente diagnosticano i problemi wireless nelle aree seguenti.

-   Eventuali problemi di connettività 802.11, tra cui l'associazione 802.11, l'autenticazione 802.11, le impostazioni di sicurezza 802.11 correlate agli standard 802.11 & protocolli supportati in modo nativo nel sistema operativo e problemi di prestazioni.
-   Problemi di sicurezza di livello 2 relativi alle configurazioni 802.1x ed eventuali problemi relativi all'autenticazione di livello 2 tramite metodi supportati in modo nativo in Windows Vista e Windows Server 2008.
-   Mancata corrispondenza della configurazione nelle impostazioni del profilo tra il client e il punto di accesso o l'infrastruttura e i servizi di rete.

Le classi helper di diagnostica wireless 802.11 attualmente non diagnosticano i problemi wireless nelle aree seguenti.

-   Problemi relativi alle estensioni 802.11 di terze parti, incluse eventuali impostazioni del profilo o del driver correlate a tali estensioni.
-   Problemi relativi ai metodi EAP di terze parti.
-   Problemi relativi al driver miniport wireless.
-   Eventuali problemi relativi al protocollo di sicurezza 802.11 e di livello 2 o agli standard non supportati in modo nativo.
-   Problemi a livello di sistema o di componente che potrebbero influire sulla connettività wireless, ad esempio risparmio energia, spazio su disco insufficiente, condizioni di memoria e problemi hardware.

Inoltre, diagnostica wireless 802.11 non analizza [**i casi di utilizzo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-highutilization) elevato. I problemi di prestazioni wireless identificati verranno analizzati e segnalati come [**casi lowhealth.**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth)

 

 




