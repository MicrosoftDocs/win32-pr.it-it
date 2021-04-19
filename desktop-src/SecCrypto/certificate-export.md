---
description: Copia un certificato in una stringa codificata.
ms.assetid: bae7fb57-6b44-4aac-a635-b5b82de1f68d
title: 'Metodo ICertificate2:: Export'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Export
- ICertificate2.Export
- ICertificate.Export
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: aee48fe3d9ba56cba90c9645a3fb9752e3367a20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332156"
---
# <a name="icertificate2export-method"></a>Metodo ICertificate2:: Export

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Il metodo **Export** copia un certificato in una stringa codificata. La stringa codificata può essere scritta in un file o importata in un nuovo oggetto [**certificato**](certificate.md) .

## <a name="syntax"></a>Sintassi


```VB
Certificate.Export( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*EncodingType* \[ in, facoltativo\]
</dt> <dd>

Valore dell'enumerazione del [**\_ \_ tipo di codifica CAPICOM**](capicom-encoding-type.md) che specifica il tipo di codifica per l'operazione di esportazione. Il valore predefinito è **CAPICOM \_ Encode \_ base64**. Nella tabella seguente sono illustrati i possibili valori.



| Valore                                                                                                                                                                                  | Significato                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ Encode \_ any**</dt> </dl>          | Questo tipo di codifica viene utilizzato solo quando i dati di input hanno un tipo di codifica sconosciuto. Se questo valore viene usato per specificare il tipo di codifica dell'output, \_ \_ verrà invece usato CAPICOM Encode Base64. Introdotta in capicol 2,0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**\_Codifica Base64 per CAPICOM \_**</dt> </dl> | I dati vengono salvati come stringa con codifica Base64.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**\_codificare il \_ file binario di CAPICOM**</dt> </dl> | I dati vengono salvati come una sequenza binaria pura.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Stringa che contiene il certificato esportato nel formato di codifica specificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti Cryptography](cryptography-objects.md)
</dt> <dt>

[**Certificato**](certificate.md)
</dt> </dl>

 

 
