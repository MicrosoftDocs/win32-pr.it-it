---
description: Visualizza una finestra di dialogo per la selezione dei certificati e restituisce una raccolta di tali certificati selezionati.
ms.assetid: dbf49a4b-6da1-4819-afcd-46db89a00fce
title: Metodo ICertificates2::Select
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Select
- ICertificates2.Select
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 50e10a9487318c7b89e89afb3d10d5974524c821b76618ca8ffd1f282e844f65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770486"
---
# <a name="icertificates2select-method"></a>Metodo ICertificates2::Select

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Il **metodo Select** visualizza una finestra di dialogo per la selezione dei certificati e restituisce una raccolta di tali certificati selezionati. Questo metodo è stato introdotto in CAPICOM 2.0.

## <a name="syntax"></a>Sintassi


```VB
Certificates.Select( _
  [ ByVal Title ], _
  [ ByVal DisplayString ], _
  [ ByVal bMultiSelect ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Titolo* \[ in, facoltativo\]
</dt> <dd>

Stringa contenente il titolo della finestra di dialogo. Il valore predefinito è una stringa vuota ("").

</dd> <dt>

*DisplayString* \[ in, facoltativo\]
</dt> <dd>

Stringa contenente il testo del prompt visualizzato con la finestra di dialogo. Il valore predefinito è una stringa vuota ("").

</dd> <dt>

*bMultiSelect* \[ in, facoltativo\]
</dt> <dd>

Valore booleano che indica se l'utente può selezionare più di un certificato. True indica che è possibile selezionare più certificati usando CTRL o MAIUSC. Il valore predefinito è false.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Oggetto [**Certificates**](certificates.md) che contiene i certificati selezionati dalla finestra di dialogo.

**CAPICOM 2.1:** [**L'oggetto**](certificates.md) Certificates restituito contiene riferimenti ai certificati nella raccolta da cui è stata effettuata la selezione. Tutte le modifiche apportate ai certificati nell'oggetto **Certificates** restituito vengono riflesse in tale raccolta.

**CAPICOM 2.0, CAPICOM 2.0.0.1, CAPICOM 2.0.0.2 e CAPICOM 2.0.0.3:** [**L'oggetto**](certificates.md) Certificates restituito contiene copie dei certificati nella raccolta da cui è stata effettuata la selezione. Tutte le modifiche apportate ai certificati nell'oggetto **Certificates** restituito non vengono riflesse in tale raccolta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
