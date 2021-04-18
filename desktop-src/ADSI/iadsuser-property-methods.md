---
title: Metodi di proprietà IADsUser (IADs. h)
description: I metodi di proprietà dell'interfaccia IADsUser ottengono o impostano le proprietà descritte nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: 02d0e5f1-8bc9-4ef6-962d-432654ca8433
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsUser ADSI
topic_type:
- apiref
api_name:
- IADsUser Property Methods
- IADsUser.AccountDisabled
- IADsUser.get_AccountDisabled
- IADsUser.put_AccountDisabled
- IADsUser.AccountExpirationDate
- IADsUser.get_AccountExpirationDate
- IADsUser.put_AccountExpirationDate
- IADsUser.BadLoginAddress
- IADsUser.get_BadLoginAddress
- IADsUser.BadLoginCount
- IADsUser.get_BadLoginCount
- IADsUser.Department
- IADsUser.get_Department
- IADsUser.put_Department
- IADsUser.Description
- IADsUser.get_Description
- IADsUser.put_Description
- IADsUser.Division
- IADsUser.get_Division
- IADsUser.put_Division
- IADsUser.EmailAddress
- IADsUser.get_EmailAddress
- IADsUser.put_EmailAddress
- IADsUser.EmployeeID
- IADsUser.get_EmployeeID
- IADsUser.put_EmployeeID
- IADsUser.FaxNumber
- IADsUser.get_FaxNumber
- IADsUser.put_FaxNumber
- IADsUser.FirstName
- IADsUser.get_FirstName
- IADsUser.put_FirstName
- IADsUser.FullName
- IADsUser.get_FullName
- IADsUser.put_FullName
- IADsUser.GraceLoginsAllowed
- IADsUser.get_GraceLoginsAllowed
- IADsUser.put_GraceLoginsAllowed
- IADsUser.GraceLoginsRemaining
- IADsUser.get_GraceLoginsRemaining
- IADsUser.put_GraceLoginsRemaining
- IADsUser.HomeDirectory
- IADsUser.get_HomeDirectory
- IADsUser.put_HomeDirectory
- IADsUser.HomePage
- IADsUser.get_HomePage
- IADsUser.put_HomePage
- IADsUser.IsAccountLocked
- IADsUser.get_IsAccountLocked
- IADsUser.put_IsAccountLocked
- IADsUser.Languages
- IADsUser.get_Languages
- IADsUser.put_Languages
- IADsUser.LastFailedLogin
- IADsUser.get_LastFailedLogin
- IADsUser.LastLogin
- IADsUser.get_LastLogin
- IADsUser.LastLogoff
- IADsUser.get_LastLogoff
- IADsUser.LastName
- IADsUser.get_LastName
- IADsUser.put_LastName
- IADsUser.LoginHours
- IADsUser.get_LoginHours
- IADsUser.put_LoginHours
- IADsUser.LoginScript
- IADsUser.get_LoginScript
- IADsUser.put_LoginScript
- IADsUser.LoginWorkstations
- IADsUser.get_LoginWorkstations
- IADsUser.put_LoginWorkstations
- IADsUser.Manager
- IADsUser.get_Manager
- IADsUser.put_Manager
- IADsUser.MaxLogins
- IADsUser.get_MaxLogins
- IADsUser.put_MaxLogins
- IADsUser.MaxStorage
- IADsUser.get_MaxStorage
- IADsUser.put_MaxStorage
- IADsUser.NamePrefix
- IADsUser.get_NamePrefix
- IADsUser.put_NamePrefix
- IADsUser.NameSuffix
- IADsUser.get_NameSuffix
- IADsUser.put_NameSuffix
- IADsUser.OfficeLocations
- IADsUser.get_OfficeLocations
- IADsUser.put_OfficeLocations
- IADsUser.OtherName
- IADsUser.get_OtherName
- IADsUser.put_OtherName
- IADsUser.PasswordExpirationDate
- IADsUser.get_PasswordExpirationDate
- IADsUser.put_PasswordExpirationDate
- IADsUser.PasswordLastChanged
- IADsUser.get_PasswordLastChanged
- IADsUser.PasswordMinimumLength
- IADsUser.get_PasswordMinimumLength
- IADsUser.put_PasswordMinimumLength
- IADsUser.PasswordRequired
- IADsUser.get_PasswordRequired
- IADsUser.put_PasswordRequired
- IADsUser.Picture
- IADsUser.get_Picture
- IADsUser.put_Picture
- IADsUser.PostalAddresses
- IADsUser.get_PostalAddresses
- IADsUser.put_PostalAddresses
- IADsUser.PostalCodes
- IADsUser.get_PostalCodes
- IADsUser.put_PostalCodes
- IADsUser.Profile
- IADsUser.get_Profile
- IADsUser.put_Profile
- IADsUser.RequireUniquePassword
- IADsUser.get_RequireUniquePassword
- IADsUser.put_RequireUniquePassword
- IADsUser.SeeAlso
- IADsUser.get_SeeAlso
- IADsUser.put_SeeAlso
- IADsUser.TelephoneHome
- IADsUser.get_TelephoneHome
- IADsUser.put_TelephoneHome
- IADsUser.TelephoneMobile
- IADsUser.get_TelephoneMobile
- IADsUser.put_TelephoneMobile
- IADsUser.TelephoneNumber
- IADsUser.get_TelephoneNumber
- IADsUser.put_TelephoneNumber
- IADsUser.TelephonePager
- IADsUser.get_TelephonePager
- IADsUser.put_TelephonePager
- IADsUser.Title
- IADsUser.get_Title
- IADsUser.put_Title
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6689776fe1ce9102ed4bb8ad97252be41901a0ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301085"
---
# <a name="iadsuser-property-methods"></a>Metodi di proprietà IADsUser

I metodi di proprietà dell'interfaccia [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) ottengono o impostano le proprietà descritte nella tabella seguente. Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).

## <a name="properties"></a>Proprietà

<dl> <dt>

**AccountDisabled**
</dt> <dd> <dl>

Flag che indica se l'account è o deve essere disabilitato.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Boolean**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AccountDisabled(
  [out] VARIANT_BOOL* pfAccountDisabled
);
HRESULT put_AccountDisabled(
  [in] VARIANT_BOOL fAccountDisabled
);
```


</dt> </dl> </dd> <dt>

**AccountExpirationDate**
</dt> <dd> <dl>

Data e ora in cui l'utente non può effettuare l'accesso.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **date**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AccountExpirationDate(
  [out] DATE* pdateAccountExpirationDate
);
HRESULT put_AccountExpirationDate(
  [in] DATE dateAccountExpirationDate
);
```


</dt> </dl> </dd> <dt>

**BadLoginAddress**
</dt> <dd> <dl>

Ultimo nodo considerato un possibile intruso; Questa operazione è disponibile se è attivo il rilevamento di intrusi.

<dt>

Tipo di accesso: sola lettura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_BadLoginAddress(
  [out] BSTR* pbstrBadLoginAddress
);
```


</dt> </dl> </dd> <dt>

**BadLoginCount**
</dt> <dd> <dl>

Numero di tentativi di accesso non validi dall'ultima reimpostazione.

<dt>

Tipo di accesso: sola lettura
</dt> <dt>

Tipo di dati di scripting: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_BadLoginCount(
  [out] LONG* plBadLoginCount
);
```


</dt> </dl> </dd> <dt>

**Reparto**
</dt> <dd> <dl>

Reparto, unità organizzativa, all'interno dell'azienda a cui appartiene l'utente.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Department(
  [out] BSTR* pbstrDepartment
);
HRESULT put_Department(
  [in] BSTR bstrDepartment
);
```


</dt> </dl> </dd> <dt>

**Descrizione**
</dt> <dd> <dl>

Descrizione del testo dell'utente.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> <dt>

**Divisione**
</dt> <dd> <dl>

Divisione all'interno di una società o organizzazione.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Division(
  [out] BSTR* pbstrDivision
);
HRESULT put_Division(
  [in] BSTR bstrDivision
);
```


</dt> </dl> </dd> <dt>

**EmailAddress**
</dt> <dd> <dl>

Indirizzo di posta elettronica dell'utente.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_EmailAddress(
  [out] BSTR* pbstrEmailAddress
);
HRESULT put_EmailAddress(
  [in] BSTR bstrEmailAddress
);
```


</dt> </dl> </dd> <dt>

**EmployeeID**
</dt> <dd> <dl>

Identificatore del dipendente dell'utente.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_EmployeeID(
  [out] BSTR* pbstrEmployeeID
);
HRESULT put_EmployeeID(
  [in] BSTR bstrEmployeeID
);
```


</dt> </dl> </dd> <dt>

**NumeroFax**
</dt> <dd> <dl>

Numero di fax, o numeri, dell'utente. In Active Directory questa proprietà è a valore singolo e la matrice **Variant** ha un solo elemento.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_FaxNumber(
  [out] VARIANT* pvarFaxNumber
);
HRESULT put_FaxNumber(
  [in] VARIANT varFaxNumber
);
```


</dt> </dl> </dd> <dt>

**FirstName**
</dt> <dd> <dl>

Nome dell'utente.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_FirstName(
  [out] BSTR* pbstrFirstName
);
HRESULT put_FirstName(
  [in] BSTR bstrFirstName
);
```


</dt> </dl> </dd> <dt>

**FullName**
</dt> <dd> <dl>

Nome completo dell'utente.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_FullName(
  [out] BSTR* pbstrFullName
);
HRESULT put_FullName(
  [in] BSTR bstrFullName
);
```


</dt> </dl> </dd> <dt>

**GraceLoginsAllowed**
</dt> <dd> <dl>

Il numero di volte in cui l'utente può accedere dopo la scadenza della password.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_GraceLoginsAllowed(
  [out] LONG* plGraceLoginsAllowed
);
HRESULT put_GraceLoginsAllowed(
  [in] LONG lGraceLoginsAllowed
);
```


</dt> </dl> </dd> <dt>

**GraceLoginsRemaining**
</dt> <dd> <dl>

Numero di accessi consentiti prima del blocco dell'account.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_GraceLoginsRemaining(
  [out] LONG* plGraceLoginsRemaining
);
HRESULT put_GraceLoginsRemaining(
  [in] LONG lGraceLoginsRemaining
);
```


</dt> </dl> </dd> <dt>

**HomeDirectory**
</dt> <dd> <dl>

La home directory dell'utente.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HomeDirectory(
  [out] BSTR* pbstrHomeDirectory
);
HRESULT put_HomeDirectory(
  [in] BSTR bstrHomeDirectory
);
```


</dt> </dl> </dd> <dt>

**Home page**
</dt> <dd> <dl>

URL per il home page dell'utente.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HomePage(
  [out] BSTR* pbstrHomePage
);
HRESULT put_HomePage(
  [in] BSTR bstrHomePage
);
```


</dt> </dl> </dd> <dt>

**IsAccountLocked**
</dt> <dd> <dl>

Flag che indica se l'account è bloccato a causa del rilevamento di intrusioni. Questa proprietà ha un utilizzo limitato quando viene usata con il provider ADSI LDAP. Per ulteriori informazioni su queste limitazioni, vedere [blocco degli account (provider LDAP)](ldap-account-lockout.md).

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Boolean**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IsAccountLocked(
  [out] VARIANT_BOOL* pfIsAccountLocked
);
HRESULT put_IsAccountLocked(
  [in] VARIANT_BOOL fIsAccountLocked
);
```


</dt> </dl> </dd> <dt>

**Linguaggi**
</dt> <dd> <dl>

Matrice di nomi di lingua **BSTR** per l'utente.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Languages(
  [out] VARIANT* pvLanguages
);
HRESULT put_Languages(
  [in] VARIANT vLanguages
);
```


</dt> </dl> </dd> <dt>

**LastFailedLogin**
</dt> <dd> <dl>

Data e ora dell'ultimo accesso di rete non riuscito.

<dt>

Tipo di accesso: sola lettura
</dt> <dt>

Tipo di dati di scripting: **date**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LastFailedLogin(
  [out] DATE* pdateLastFailedLogin
);
```


</dt> </dl> </dd> <dt>

**LastLogin**
</dt> <dd> <dl>

Data e ora dell'ultimo accesso di rete.

<dt>

Tipo di accesso: sola lettura
</dt> <dt>

Tipo di dati di scripting: **date**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LastLogin(
  [out] DATE* pdateLastLogin
);
```


</dt> </dl> </dd> <dt>

**LastLogoff**
</dt> <dd> <dl>

Data e ora dell'ultima disconnessione di rete.

<dt>

Tipo di accesso: sola lettura
</dt> <dt>

Tipo di dati di scripting: **date**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LastLogoff(
  [out] DATE* pdateLastLogoff
);
```


</dt> </dl> </dd> <dt>

**LastName**
</dt> <dd> <dl>

Cognome dell'utente.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LastName(
  [out] BSTR* pbstrLastName
);
HRESULT put_LastName(
  [in] BSTR bstrLastName
);
```


</dt> </dl> </dd> <dt>

**LoginHours**
</dt> <dd> <dl>

Periodi di tempo per ogni giorno della settimana durante i quali sono consentiti gli accessi per l'utente. Rappresentata come una tabella di valori booleani per la settimana, ognuno dei quali indica se lo slot di tempo è un orario di accesso valido. Tenere presente che la rappresentazione è specifica del provider e della directory.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LoginHours(
  [out] VARIANT* pvLoginHours
);
HRESULT put_LoginHours(
  [in] VARIANT vLoginHours
);
```


</dt> </dl> </dd> <dt>

**LoginScript**
</dt> <dd> <dl>

Percorso dello script di accesso.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LoginScript(
  [out] BSTR* pbstrLoginScript
);
HRESULT put_LoginScript(
  [in] BSTR bstrLoginScript
);
```


</dt> </dl> </dd> <dt>

**LoginWorkstations**
</dt> <dd> <dl>

Indirizzi o nomi di workstation, del tipo di dati **BSTR** , da cui l'utente può effettuare l'accesso.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LoginWorkstations(
  [out] VARIANT* pvLoginWorkstations
);
HRESULT put_LoginWorkstations(
  [in] VARIANT vLoginWorkstations
);
```


</dt> </dl> </dd> <dt>

**Responsabile**
</dt> <dd> <dl>

Gestore dell'utente.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Manager(
  [out] BSTR* pbstrManager
);
HRESULT put_Manager(
  [in] BSTR bstrManager
);
```


</dt> </dl> </dd> <dt>

**MaxLogins**
</dt> <dd> <dl>

Numero di sessioni di accesso simultanee consentite.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxLogins(
  [out] LONG* plMaxLogins
);
HRESULT put_MaxLogins(
  [in] LONG lMaxLogins
);
```


</dt> </dl> </dd> <dt>

**MaxStorage**
</dt> <dd> <dl>

Quantità massima di spazio su disco, espressa in kilobyte, che può essere utilizzata dall'utente.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxStorage(
  [out] LONG* plMaxStorage
);
HRESULT put_MaxStorage(
  [in] LONG lMaxStorage
);
```


</dt> </dl> </dd> <dt>

**NamePrefix**
</dt> <dd> <dl>

Prefisso del nome dell'utente, ad esempio "ms." o "Hon".

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NamePrefix(
  [out] BSTR* pbstrNamePrefix
);
HRESULT put_NamePrefix(
  [in] BSTR bstrNamePrefix
);
```


</dt> </dl> </dd> <dt>

**NameSuffix**
</dt> <dd> <dl>

Suffisso del nome dell'utente, ad esempio "Jr." o "III".

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NameSuffix(
  [out] BSTR* pbstrNameSuffix
);
HRESULT put_NameSuffix(
  [in] BSTR bstrNameSuffix
);
```


</dt> </dl> </dd> <dt>

**OfficeLocations**
</dt> <dd> <dl>

Posizione dell'ufficio come matrice **BSTR** per l'utente. Per Active Directory, questa proprietà è a valore singolo e la matrice contiene un elemento.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OfficeLocations(
  [out] VARIANT* pvOfficeLocations
);
HRESULT put_OfficeLocations(
  [in] VARIANT vOfficeLocations
);
```


</dt> </dl> </dd> <dt>

**UPN**
</dt> <dd> <dl>

Nome aggiuntivo, ad esempio, il secondo nome per l'utente.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OtherName(
  [out] BSTR* pbstrOtherName
);
HRESULT put_OtherName(
  [in] BSTR bstrOtherName
);
```


</dt> </dl> </dd> <dt>

**PasswordExpirationDate**
</dt> <dd> <dl>

Data e ora di scadenza della password.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **date**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PasswordExpirationDate(
  [out] DATE* pdatePasswordExpirationDate
);
HRESULT put_PasswordExpirationDate(
  [in] DATE datePasswordExpirationDate
);
```


</dt> </dl> </dd> <dt>

**PasswordLastChanged**
</dt> <dd> <dl>

Data e ora dell'Ultima modifica della password.

<dt>

Tipo di accesso: sola lettura
</dt> <dt>

Tipo di dati di scripting: **date**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PasswordLastChanged(
  [out] DATE* pdatePasswordLastChanged
);
```


</dt> </dl> </dd> <dt>

**PasswordMinimumLength**
</dt> <dd> <dl>

Lunghezza minima della password.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PasswordMinimumLength(
  [out] LONG* plPasswordMinimumLength
);
HRESULT put_PasswordMinimumLength(
  [in] LONG lPasswordMinimumLength
);
```


</dt> </dl> </dd> <dt>

**PasswordRequired**
</dt> <dd> <dl>

Flag che indica se la password è obbligatoria.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Boolean**
</dt> <dt>



``` syntax
// C++ method syntax
VARIANT_BOOL get_PasswordRequired(
  [out] VARIANT_BOOL* pfPasswordRequired
);
HRESULT put_PasswordRequired(
  [in] VARIANT_BOOL fPasswordRequired
);
```


</dt> </dl> </dd> <dt>

**Immagine**
</dt> <dd> <dl>

Matrice OctetString di byte in cui è archiviata un'immagine.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Picture(
  [out] VARIANT* pvarPicture
);
HRESULT put_Picture(
  [in] VARIANT varPicture
);
```


</dt> </dl> </dd> <dt>

**PostalAddresses**
</dt> <dd> <dl>

Indirizzo postale come matrice **BSTR** . Questa proprietà è multivalore per mantenere più di indirizzi dell'utente. Il formato interno di una PostalAddress deve essere conforme a CCITT F. 401 come a cui viene fatto riferimento in X. 521-1993, che definisce un PostalAddress come sei elementi di 30 byte ciascuno, che contiene un indirizzo via (facoltativamente) Post Office, città o località, stato o provincia, CAP e paese/area geografica.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PostalAddresses(
  [out] VARIANT* pvPostalAddresses
);
HRESULT put_PostalAddresses(
  [in] VARIANT vPostalAddresses
);
```


</dt> </dl> </dd> <dt>

**PostalCodes**
</dt> <dd> <dl>

Cap come matrice **BSTR** . I codici postali sono collegati in modo posizionale alla matrice **PostalAddresses** . In Active Directory, tuttavia, questa proprietà è a valore singolo e la matrice ha un singolo elemento.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PostalCodes(
  [out] VARIANT* pvPostalCodes
);
HRESULT put_PostalCodes(
  [in] VARIANT vPostalCodes
);
```


</dt> </dl> </dd> <dt>

**Profilo**
</dt> <dd> <dl>

Percorso del profilo utente.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Profile(
  [out] BSTR* pbstrProfile
);
HRESULT put_Profile(
  [in] BSTR bstrProfile
);
```


</dt> </dl> </dd> <dt>

**RequireUniquePassword**
</dt> <dd> <dl>

Flag che indica se una nuova password deve essere diversa da quelle note tramite una cronologia delle password.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Boolean**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_RequireUniquePassword(
  [out] VARIANT_BOOL* pfRequireUniquePassword
);
HRESULT put_RequireUniquePassword(
  [in] VARIANT_BOOL fRequireUniquePassword
);
```


</dt> </dl> </dd> <dt>

**SeeAlso**
</dt> <dd> <dl>

Matrice di ADsPaths di altri oggetti correlati all'utente.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SeeAlso(
  [out] VARIANT* pvSeeAlso
);
HRESULT put_SeeAlso(
  [in] VARIANT vSeeAlso
);
```


</dt> </dl> </dd> <dt>

**TelephoneHome**
</dt> <dd> <dl>

Una matrice di numeri di telefono di casa dell'utente. In Active Directory questa proprietà è a valore singolo e la matrice contiene un elemento.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TelephoneHome(
  [out] VARIANT* pvarTelephoneHome
);
HRESULT put_TelephoneHome(
  [in] VARIANT varTelephoneHome
);
```


</dt> </dl> </dd> <dt>

**TelephoneMobile**
</dt> <dd> <dl>

Una matrice di numeri di telefono cellulare dell'utente. In Active Directory questa proprietà è a valore singolo e la matrice ha un solo elemento.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TelephoneMobile(
  [out] VARIANT* pvarTelephoneMobile
);
HRESULT put_TelephoneMobile(
  [in] VARIANT varTelephoneMobile
);
```


</dt> </dl> </dd> <dt>

**TelephoneNumber**
</dt> <dd> <dl>

Matrice di numeri di telefono, in genere correlati al lavoro, associati all'utente. In Active Directory questa proprietà è a valore singolo e la matrice è di un singolo elemento.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TelephoneNumber(
  [out] VARIANT* pvarTelephoneNumber
);
HRESULT put_TelephoneNumber(
  [in] VARIANT varTelephoneNumber
);
```


</dt> </dl> </dd> <dt>

**TelephonePager**
</dt> <dd> <dl>

Matrice di numeri di cercapersone dell'utente. In Active Directory questa proprietà è a valore singolo e la matrice è di un singolo elemento.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TelephonePager(
  [out] VARIANT* pvarTelephonePager
);
HRESULT put_TelephonePager(
  [in] VARIANT varTelephonePager
);
```


</dt> </dl> </dd> <dt>

**Title**
</dt> <dd> <dl>

Titolo dell'utente.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Title(
  [out] BSTR* pbstrTitle
);
HRESULT put_Title(
  [in] BSTR bstrTitle
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Commenti

Il provider WinNT fornito da Microsoft non supporta tutti i metodi di proprietà [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) , come illustrato in precedenza. Tuttavia, il provider supporta altre proprietà a cui è possibile accedere tramite il metodo [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) o [**IADs::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put) . Per ulteriori informazioni e per un elenco di proprietà non supportate ed esempi di codice, vedere [oggetto utente WinNT](winnt-user-object.md) nel [provider ADSI WinNT](adsi-winnt-provider.md).

Per ulteriori informazioni sulle funzionalità specifiche del provider LDAP ADSI dell'oggetto classe utente, vedere [oggetto utente LDAP](ldap-user-object.md) nel [provider LDAP ADSI](adsi-ldap-provider.md). Questo argomento include [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser), oltre a esempi di codice per la gestione di un account utente.

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene illustrato come eseguire l'associazione a un oggetto account utente e recuperare il nome completo dell'utente.


```VB
Dim usr As IADsUser
Dim sFullName as String

On Error GoTo Cleanup
Set usr = GetObject("WinNT://Fabrikam/JeffSmith,user")
sFullName = usr.FullName

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set usr = Nothing
```



Nell'esempio di codice seguente viene illustrato come eseguire l'associazione a un oggetto account utente e recuperare il nome completo dell'utente.


```C++
IADsUser *GetUserObject(LPWSTR uPath)
{
    IADsUser *pUser;
    HRESULT hr = ADsGetObject(uPath,IID_IADsUser,(void**)&pUser);
    if (FAILED(hr)) {return NULL;}
    BSTR bstr;
    hr = pUser->get_FullName(&bstr);
    printf("User: %S\n", bstr);
    SysFreeString(bstr);
    return pUser;
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsUser è definito come 3E37E320-17E2-11CF-ABC4-02608C9E7553<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser)
</dt> <dt>

[Metodi di proprietà dell'interfaccia](interface-property-methods.md)
</dt> <dt>

[**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get)
</dt> <dt>

[**IADs::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put)
</dt> <dt>

[Oggetto utente WinNT](winnt-user-object.md)
</dt> <dt>

[Provider ADSI WinNT](adsi-winnt-provider.md)
</dt> <dt>

[Oggetto utente LDAP](ldap-user-object.md)
</dt> <dt>

[Provider LDAP ADSI](adsi-ldap-provider.md)
</dt> </dl>

 

 





