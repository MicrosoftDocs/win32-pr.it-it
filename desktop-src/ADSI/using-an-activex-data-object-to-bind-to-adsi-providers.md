---
title: Utilizzo di un oggetto dati ActiveX per l'associazione a provider ADSI
description: Poiché ADSI è anche un provider di OLE DB, è possibile utilizzare un oggetto ADO (ActiveX Data Object) per connettersi ai provider ADSI.
ms.assetid: b42d804b-f1eb-4085-88aa-015a92309ee8
ms.tgt_platform: multiple
keywords:
- ActiveX Data Object ADSI
- ActiveX Data Object ADSI, utilizzo di ADO per l'associazione a provider ADSI
- provider di servizi ADSI, utilizzo dell'oggetto dati ActiveX per l'associazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4efb64da28d5c4c2596fcf889e3b3db88b77205c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044047"
---
# <a name="using-an-activex-data-object-to-bind-to-adsi-providers"></a>Utilizzo di un oggetto dati ActiveX per l'associazione a provider ADSI

Poiché ADSI è anche un provider di OLE DB, è possibile utilizzare un oggetto ADO (ActiveX Data Object) per connettersi ai provider ADSI. Come per gli altri provider ADO, per connettersi a un provider di OLE DB, è necessario creare un nuovo oggetto connessione e, facoltativamente, specificare le credenziali. Il nome del provider OLE DB ADSI è **ADSDSOObject**.

Ad esempio:


```VB
Dim con As New Connection 
'VBScript use: con = CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
con.Open "YourDescriptionHere"
```



Nell'esempio precedente si è connessi per conto dell'utente corrente. Per specificare credenziali diverse, utilizzare le proprietà di connessione:


```VB
con.Provider = "ADsDSOObject"
con.Properties("User ID") = "jeffsmith"
con.Properties("Password") = "guesswhat?"
con.Properties("Encrypt Password") = True
con.Open "YourDescriptionHere"
```



ADSI OLE DB definisce le proprietà di connessione seguenti.



| Proprietà           | Tipo di dati   | Predefinito   |
|--------------------|-------------|-----------|
| "User ID"          | **BSTR**    | **NULL**  |
| "Password"         | **BSTR**    | **NULL**  |
| "Crittografa password" | **BOOLEAN** | **FALSE** |
| "Flag ADSI"        | **Long**    | 0         |



 

Utilizzando OLE DB ADO, non è possibile eseguire l'associazione a un oggetto specifico. È tuttavia possibile eseguire una query su un oggetto specifico e ottenere un set di risultati. Solo i provider ADSI che supportano [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) traggono vantaggio da ADO come modello di programmazione.

La proprietà del flag ADSI viene utilizzata per specificare l'opzione di autenticazione del binding. Questa proprietà può essere una combinazione di flag dell'enumerazione dell'enumerazione di [**\_ \_ autenticazione ADS**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) .

 

 




