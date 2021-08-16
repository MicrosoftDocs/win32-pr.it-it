---
description: Crea e aggiunge una nuova condivisione DDE alla gestione database di condivisione DDE.
ms.assetid: c9814919-412e-4f13-98cc-373b69545734
title: Funzione NDdeShareAdd (Nddeapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareAdd
- NDdeShareAddA
- NDdeShareAddW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 0a02381fad8412c7ada0c337c21e633ffa6793887a720ec504f1dfa3d78d9ede
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602141"
---
# <a name="nddeshareadd-function"></a>Funzione NDdeShareAdd

\[DDE di rete non è più supportato. Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ NOT \_ IMPLEMENTED.\]

Crea e aggiunge una nuova condivisione DDE alla gestione database di condivisione DDE.

## <a name="syntax"></a>Sintassi


```C++
UINT NDdeShareAdd(
  _In_ LPTSTR               lpszServer,
  _In_ UINT                 nLevel,
  _In_ PSECURITY_DESCRIPTOR pSD,
  _In_ LPBYTE               lpBuffer,
  _In_ DWORD                cBufSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpszServer* \[ Pollici\]
</dt> <dd>

Nome del server il cui DSDM deve essere modificato.

</dd> <dt>

*nLevel* \[ Pollici\]
</dt> <dd>

Livello di informazioni. Questo parametro deve essere 2.

</dd> <dt>

*pSD* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura SECURITY \_ DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) da associare a questa condivisione e rispetto alla quale verranno eseguiti i controlli di accesso agli avvii successivi di questa condivisione. Questo parametro può essere **NULL,** nel qual caso DSDM crea un descrittore di sicurezza predefinito che concede "Controllo completo" al proprietario e "Lettura e collegamento" a tutti.

</dd> <dt>

*lpBuffer* \[in\]
</dt> <dd>

Puntatore alla [**struttura NDDESHAREINFO**](nddeshareinfo-str.md) che definisce l'elenco ApplicationTopic associato alla condivisione DDE creata e ad altri parametri. Questo parametro non può essere **NULL.**

</dd> <dt>

*cBufSize* \[ Pollici\]
</dt> <dd>

Dimensioni della struttura *lpBuffer,* in byte. Questo parametro non può essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NDDE \_ NO \_ ERROR.

Se la funzione ha esito negativo, il valore restituito è un codice di errore, che può essere convertito in un messaggio di errore di testo chiamando [**NDdeGetErrorString.**](nddegeterrorstring.md)

## <a name="remarks"></a>Commenti

Prima che un client possa connettersi alla condivisione DDE, deve essere considerato attendibile con [**NDdeSetTrustedShare.**](nddesettrustedshare.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **NDdeShareAddW** (Unicode) e **NDdeShareAddA** (ANSI)<br/>                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica delle Dynamic Data Exchange rete](network-dynamic-data-exchange.md)
</dt> <dt>

[Funzioni DDE di rete](network-dde-functions.md)
</dt> <dt>

[**NDDESHAREINFO**](nddeshareinfo-str.md)
</dt> <dt>

[**NDdeSetTrustedShare**](nddesettrustedshare.md)
</dt> </dl>

 

