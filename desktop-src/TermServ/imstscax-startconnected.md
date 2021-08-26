---
title: Proprietà IMsTscAx StartConnected
description: Indica se il controllo stabilirà la connessione Desktop remoto server host sessione Desktop remoto immediatamente all'avvio.
ms.assetid: cf2956c0-be4f-4f80-a14b-253ae8117824
ms.tgt_platform: multiple
keywords:
- Proprietà StartConnected Servizi Desktop remoto
- Proprietà StartConnected Servizi Desktop remoto, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto , proprietà StartConnected
- Proprietà StartConnected Servizi Desktop remoto, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto proprietà StartConnected
- Proprietà StartConnected Servizi Desktop remoto, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto , proprietà StartConnected
- Proprietà StartConnected Servizi Desktop remoto, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto , proprietà StartConnected
- Proprietà StartConnected Servizi Desktop remoto, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto , proprietà StartConnected
- Proprietà StartConnected Servizi Desktop remoto, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto , proprietà StartConnected
- Proprietà StartConnected Servizi Desktop remoto, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto , proprietà StartConnected
- Proprietà StartConnected Servizi Desktop remoto, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto , proprietà StartConnected
- Proprietà StartConnected Servizi Desktop remoto, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto , proprietà StartConnected
- Proprietà StartConnected Servizi Desktop remoto, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto , proprietà StartConnected
topic_type:
- apiref
api_name:
- IMsTscAx.StartConnected
- IMsTscAx.get_StartConnected
- IMsTscAx.put_StartConnected
- IMsRdpClient.StartConnected
- IMsRdpClient.get_StartConnected
- IMsRdpClient.put_StartConnected
- IMsRdpClient2.StartConnected
- IMsRdpClient2.get_StartConnected
- IMsRdpClient2.put_StartConnected
- IMsRdpClient3.StartConnected
- IMsRdpClient3.get_StartConnected
- IMsRdpClient3.put_StartConnected
- IMsRdpClient4.StartConnected
- IMsRdpClient4.get_StartConnected
- IMsRdpClient4.put_StartConnected
- IMsRdpClient5.StartConnected
- IMsRdpClient5.get_StartConnected
- IMsRdpClient5.put_StartConnected
- IMsRdpClient6.StartConnected
- IMsRdpClient6.get_StartConnected
- IMsRdpClient6.put_StartConnected
- IMsRdpClient7.StartConnected
- IMsRdpClient7.get_StartConnected
- IMsRdpClient7.put_StartConnected
- IMsRdpClient8.StartConnected
- IMsRdpClient8.get_StartConnected
- IMsRdpClient8.put_StartConnected
- IMsRdpClient9.StartConnected
- IMsRdpClient9.get_StartConnected
- IMsRdpClient9.put_StartConnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bdae5535d079335354306e47ed8378fa09450d9
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880060"
---
# <a name="imstscaxstartconnected-property"></a>Proprietà IMsTscAx::StartConnected

Indica se il controllo stabilirà la connessione Desktop remoto server host sessione Desktop remoto immediatamente all'avvio.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_StartConnected(
  [in]  BOOL fStartConnected
);

HRESULT get_StartConnected(
  [out] BOOL *pfStartConnected
);
```



## <a name="property-value"></a>Valore proprietà

Impostare questo parametro su **TRUE se** il controllo deve connettersi immediatamente all'avvio oppure FALSE in **caso contrario.**

## <a name="error-codes"></a>Codici di errore

Restituisce **S \_ OK in** caso di esito positivo.

## <a name="remarks"></a>Commenti

Questa proprietà è particolarmente utile quando le proprietà del controllo vengono impostate nell'elenco di parametri di un &lt; &gt; tag OBJECT, anziché tramite chiamate di script.

Questa proprietà può essere utilizzata solo se viene specificato anche il nome del server tramite la proprietà del server. Questo parametro deve essere impostato prima dell'avvio del controllo, ad esempio includerlo nell'elenco di parametri di un tag OBJECT quando si usa il controllo &lt; &gt; da una pagina Web.

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAx IID è definito come \_ 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[Incorporamento del controllo Desktop remoto ActiveX in una pagina Web](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





