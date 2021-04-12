---
title: Supporto per l'associazione anticipata
description: Nell'esempio di codice riportato di seguito viene presentato uno scenario con il supporto dell'associazione anticipata.
ms.assetid: 3ca955cc-a9cd-4309-8617-89fe50b65c3d
ms.tgt_platform: multiple
keywords:
- estensioni ADSI, supporto per l'associazione anticipata
- Binding AD, supporto dell'associazione anticipata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be6980edb0395ad0139f9cf2e4a1f9cde3ff6077
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118450"
---
# <a name="early-binding-support"></a>Supporto per l'associazione anticipata

Nell'esempio di codice riportato di seguito viene presentato uno scenario con il supporto dell'associazione anticipata.


```VB
Dim x as IADsUser
Dim y as IADsExt1
Dim z as IADsExt2
 
Set x = GetObject("LDAP://CN=JeffSmith, OU=Sales, 
                   DC=Fabrikam,DC=COM")
x.SetPassword("newPassword")
 
Set y = x
y.MyNewMethod( "\\srv\public")
y.MyProperty = "Hello World"
 
Set z = y
z.OtherMethod()
z.OtherProperty = 4362
 
Debug.Print x.LastName
 
Set z = GetObject("LDAP://CN=Jeff,OU=Engr, 
                   DC=Fabrikam,DC=COM")
z.OtherProperty = 5323
```



In questo esempio di codice due componenti di estensione estendono un oggetto **utente** . Ogni estensione pubblica una propria interfaccia. Ogni estensione non riconosce l'altra interfaccia di estensione. solo ADSI riconosce l'esistenza di entrambe le estensioni. Ogni estensione delega la relativa [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) a ADSI. ADSI funge da aggregatore per entrambe le estensioni e per qualsiasi altra estensione futura. L'esecuzione di query su un'interfaccia da qualsiasi estensione o da ADSI produce lo stesso risultato coerente.

Nella procedura riportata di seguito viene descritto come creare un'estensione.

## <a name="step-1-add-aggregation-to-your-component"></a>Passaggio 1: aggiungere l'aggregazione al componente

Seguire la specifica COM per aggiungere l'aggregazione al componente. In breve, è necessario accettare le richieste *pUnknown* al componente durante la **CreateInstance** e delegare il *pUnknown* a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) di aggregator se il componente è aggregato.

## <a name="step-2-register-your-extension"></a>Passaggio 2: registrare l'estensione

A questo punto è necessario decidere quale classe di directory estendere. Per eseguire questa operazione, è possibile utilizzare le stesse interfacce per un'interfaccia ADSI, ad esempio [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser), [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer). Gli oggetti directory vengono mantenuti nella directory, mentre l'estensione e ADSI sono in esecuzione nel computer client. Gli esempi di oggetti directory sono **User**, **computer**, **PrintQueue**, **serviceConnectionPoint** e **nTDSService**. È possibile aggiungere una nuova classe in Active Directory e creare anche una nuova estensione per questa nuova classe.

Usare le chiavi del registro di sistema per associare un nome di classe di directory ai componenti dell'estensione ADSI. La figura seguente rappresenta il layout del registro di sistema esistente, così come le nuove chiavi.

-   Una nuova chiave, denominata **Extensions**, contiene un elenco di chiavi, ognuna delle quali rappresenta una classe nella directory. Ogni classe, ad esempio **User**, **PrintQueue** o **computer**, gestisce un elenco di sottochiavi.
-   Ogni sottochiave contiene il CLSID del componente di estensione ADSI.
-   Ogni sottochiave CLSID contiene una voce di stringa che consente più valori. È consigliabile elencare solo le interfacce che fanno parte dell'aggregazione.

> [!Note]  
> Gli oggetti di estensione sono ancora necessari per registrare le chiavi COM standard.

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         ADS
            Providers
               LDAP
                  Extensions
                     ClassNameA
                        CLSID of ExtensionA1
                           Interfaces = List of interfaces
                        CLSID of ExtensionA2
                           Interfaces = List of interfaces
                     ClassNameB
                        CLSID of ExtensionB1
                           Interfaces = List of interfaces
                        CLSID of ExtensionB2
                           Interfaces = List of interfaces
```

## <a name="example"></a>Esempio

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               LDAP
                  Extensions
                     printQueue
                        {9f37f39c-6f49-11d1-8c18-00c04fd8d503}
                           Interfaces = {466841B0-E531-11d1-8718-00C04FD44407}
                                        {466841B1-E531-11d1-8718-00C04FD44407}
```

L'elenco di interfacce da extension1 può essere diverso da quello di extension2. L'oggetto, quando attivo, supporta le interfacce di Aggregator (ADSI) e tutte le interfacce fornite dagli extension1 e extension2 dell'aggregazione. La risoluzione delle interfacce in conflitto (la stessa interfaccia supportata sia da aggregator che da aggregazioni o da più aggregazioni) è determinata dalle priorità delle estensioni.

È anche possibile associare l'estensione CLSID a più nomi di classi di oggetti. Ad esempio, l'estensione può estendere sia gli oggetti **utente** che quelli di **contatto** .

> [!Note]  
> Il comportamento dell'estensione viene aggiunto in una classe per oggetto, non in un'istanza per oggetto.

 

Come procedura consigliata, registrare le estensioni, come qualsiasi altro componente COM, con una chiamata alla funzione **DllRegisterSvr** . Fornire anche una funzionalità per annullare la registrazione dell'estensione con la funzione **DllUnregisterServer** .

Nell'esempio di codice seguente viene illustrato come registrare un'estensione.


```C++
/////
// Register the class.
///////////////////////
hr = RegCreateKeyEx( HKEY_LOCAL_MACHINE,
                 _T("SOFTWARE\\Microsoft\\ADs\\Providers\\LDAP\\Extensions\\User\\{E1E3EDF8-48D1-11D2-B22B-0000F87A6B50}"),
 0,
 NULL,
 REG_OPTION_NON_VOLATILE,
 KEY_WRITE,
 NULL,
 &hKey,
 &dwDisposition );
 
///////////////////////////
// Register the Interface.
///////////////////////////
const TCHAR szIf[] = _T("{E1E3EDF7-48D1-11D2-B22B-0000F87A6B50}");
 
hr = RegSetValueEx( hKey, _T("Interfaces"), 0, REG_BINARY, (const BYTE *) szIf, sizeof(szIf) );
 
RegCloseKey(hKey);
return S_OK;
 
}
```



 

 