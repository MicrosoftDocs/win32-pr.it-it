---
description: Visualizza una finestra di dialogo per la selezione dei certificati e restituisce una raccolta di tali certificati selezionati.
ms.assetid: dbf49a4b-6da1-4819-afcd-46db89a00fce
title: 'Metodo ICertificates2:: Select'
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
ms.openlocfilehash: cfd5b1cb5e269c14e05de25262fda711549bf02d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333162"
---
# <a name="icertificates2select-method"></a>Metodo ICertificates2:: Select

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Il metodo **Select** Visualizza una finestra di dialogo per la selezione dei certificati e restituisce una raccolta di tali certificati selezionati. Questo metodo è stato introdotto in capicol 2,0.

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

Stringa che contiene il titolo della finestra di dialogo. Il valore predefinito è una stringa vuota ("").

</dd> <dt>

*DisplayString* \[ in, facoltativo\]
</dt> <dd>

Stringa che contiene il testo della richiesta visualizzato con la finestra di dialogo. Il valore predefinito è una stringa vuota ("").

</dd> <dt>

*bMultiSelect* \[ in, facoltativo\]
</dt> <dd>

Valore booleano che indica se l'utente può selezionare più di un certificato. True indica che è possibile selezionare più certificati utilizzando il tasto CTRL o MAIUSC. Il valore predefinito è false.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Oggetto [**Certificates**](certificates.md) che contiene i certificati selezionati dalla finestra di dialogo.

**Capicom 2,1:** L'oggetto [**certificati**](certificates.md) restituito contiene riferimenti ai certificati della raccolta da cui è stata effettuata la selezione. Tutte le modifiche apportate ai certificati nell'oggetto **certificati** restituiti vengono riflesse in tale raccolta.

**CApicol 2,0, CAPICOM 2.0.0.1, CAPICOM 2.0.0.2 e CApicol 2.0.0.3:** L'oggetto [**certificati**](certificates.md) restituito contiene copie dei certificati della raccolta da cui è stata effettuata la selezione. Tutte le modifiche apportate ai certificati nell'oggetto **certificati** restituiti non vengono riflesse in tale raccolta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
