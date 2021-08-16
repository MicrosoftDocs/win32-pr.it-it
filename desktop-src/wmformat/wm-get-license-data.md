---
title: WM_GET_LICENSE_DATA struttura (Drmexternals.h)
description: La struttura WM \_ GET LICENSE DATA contiene informazioni su dove acquisire una licenza \_ \_ DRM.
ms.assetid: 7e8053d5-f3f5-4519-97f5-6dbd89982f3a
keywords:
- WM_GET_LICENSE_DATA struttura windows Media Format
topic_type:
- apiref
api_name:
- WM_GET_LICENSE_DATA
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f53b6ddfd532710e712637c57785d8893d8f977807bfb45cac0fc787ccbf58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117844475"
---
# <a name="wm_get_license_data-structure"></a>Struttura \_ DEI DATI DI WM GET \_ LICENSE \_

La **struttura WM GET LICENSE \_ \_ \_ DATA** contiene informazioni su dove acquisire una [*licenza DRM.*](wmformat-glossary.md) [](wmformat-glossary.md)

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WMGetLicenseData {
  DWORD   dwSize;
  HRESULT hr;
  WCHAR   *wszURL;
  WCHAR   *wszLocalFilename;
  BYTE    *pbPostData;
  DWORD   dwPostDataSize;
} WM_GET_LICENSE_DATA;
```



## <a name="members"></a>Members

<dl> <dt>

**dwSize**
</dt> <dd>

**Valore DWORD** contenente le dimensioni della **struttura WM GET LICENSE \_ \_ \_ DATA,** in byte.

</dd> <dt>

**h**
</dt> <dd>

**Codice restituito HRESULT.**

</dd> <dt>

**wszURL**
</dt> <dd>

Stringa con terminazione Null a caratteri wide contenente l'URL di acquisizione della licenza. Usare questa stringa e la stringa **pbPostData** nell'acquisizione di licenze non invisibile all'utente.

</dd> <dt>

**wszLocalFilename**
</dt> <dd>

Stringa con terminazione Null a caratteri wide contenente una pagina HTML locale generata dal componente DRM. Quando questa stringa viene caricata in un browser, reindirizza automaticamente la richiesta HTTP all'URL di acquisizione della licenza, insieme ai dati di post necessari. L'uso di questo URL locale è ora deprecato. L'approccio consigliato consiste nell'usare **le stringhe wszURL** **e pbPostData.**

</dd> <dt>

**pbPostData**
</dt> <dd>

Puntatore a una matrice di byte contenente i dati da pubblicare nell'URL di acquisizione della licenza. È necessario aggiungere la stringa seguente all'inizio della stringa **pbPostData:** "nonsilent=1&challenge=". La stringa risultante deve quindi essere aggiunta a **wszURL** quando si forma la richiesta HTTP.

</dd> <dt>

**dwPostDataSize**
</dt> <dd>

**Valore DWORD** che indica le dimensioni di **pbPostData** senza la stringa "nonsilent=1&challenge=" a cui si fa riferimento in **pbPostData.**

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura compilata viene restituita nel *parametro pValue* del metodo [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) se **WMT \_ STATUS** è uguale a **WMT \_ NO RIGHTS \_ \_ EX** o **WMT ACQUIRE \_ \_ LICENSE.** Per gli eventi WMT NO RIGHTS EX, il membro hr sarà \_ \_ \_ NS E LICENSE  \_ \_ \_ REQUIRED, NS E LICENSE \_ \_ \_ OUTOFDATE o NS E LICENSE INCORRECT \_ \_ \_ \_ RIGHTS. Uno di questi errori indica che è necessario acquisire una nuova licenza passando all'URL nel **membro wszURL.**

Per gli eventi ACQUIRE LICENSE di WMT, il membro hr passerà la macro SUCCEEDED se \_ una licenza è stata acquisita \_ correttamente.  Se questo evento viene ricevuto dopo un tentativo di acquisizione invisibile all'utente e **hr** è uguale a NS \_ E \_ DRM LICENSE \_ NOTACQUIRED, indica che solo l'acquisizione non invisibile all'utente è supportata dal server licenze per questa \_ licenza.

L'applicazione di esempio Audioplayer illustra come usare correttamente le informazioni restituite in questa struttura.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                      |
| Versione<br/>                  | Windows Media Format 7 SDK o versioni successive dell'SDK<br/>                       |
| Intestazione<br/>                   | <dl> <dt>Drmexternals.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense)
</dt> <dt>

[**Strutture**](structures.md)
</dt> </dl>

 

 





