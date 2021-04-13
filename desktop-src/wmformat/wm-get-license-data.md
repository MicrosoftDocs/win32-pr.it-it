---
title: Struttura WM_GET_LICENSE_DATA (Drmexternals. h)
description: La \_ \_ \_ struttura dei dati di licenza WM Get contiene informazioni sulla posizione di acquisizione di una licenza DRM.
ms.assetid: 7e8053d5-f3f5-4519-97f5-6dbd89982f3a
keywords:
- Formato di Windows Media per la struttura WM_GET_LICENSE_DATA
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
ms.openlocfilehash: 4f238bea29ab7271896dc7516b6424e4cc298f5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400617"
---
# <a name="wm_get_license_data-structure"></a>WM \_ ottenere \_ la \_ struttura dei dati di licenza

La **struttura \_ \_ \_ dei dati di licenza WM Get** contiene informazioni sulla posizione di acquisizione di una [*licenza*](wmformat-glossary.md) [*DRM*](wmformat-glossary.md) .

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

**DWORD** che contiene la dimensione della struttura di **\_ dati di \_ licenza \_ WM Get** , in byte.

</dd> <dt>

**h**
</dt> <dd>

Codice restituito **HRESULT** .

</dd> <dt>

**wszURL**
</dt> <dd>

Stringa a caratteri wide con terminazione null contenente l'URL di acquisizione della licenza. Usare questa stringa e la stringa **pbPostData** nell'acquisizione di una licenza non invisibile all'utente.

</dd> <dt>

**wszLocalFilename**
</dt> <dd>

Stringa a caratteri wide con terminazione null contenente una pagina HTML locale generata dal componente DRM. Quando questa stringa viene caricata in un browser, reindirizza automaticamente la richiesta HTTP all'URL di acquisizione della licenza, insieme ai dati post necessari. L'uso di questo URL locale è ora deprecato. L'approccio consigliato consiste nell'usare le stringhe **wszURL** e **pbPostData** .

</dd> <dt>

**pbPostData**
</dt> <dd>

Puntatore a una matrice di byte che contiene i dati da inviare all'URL di acquisizione della licenza. È necessario aggiungere la stringa seguente all'inizio della stringa **pbPostData** : "nonsilent = 1&Challenge =". La stringa risultante verrà quindi aggiunta a **wszURL** quando si forma la richiesta HTTP.

</dd> <dt>

**dwPostDataSize**
</dt> <dd>

**DWORD** che indica le dimensioni di **pbPostData** senza la stringa "nonsilent = 1&Challenge =" a cui si fa riferimento in **pbPostData**.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura compilata viene restituita nel parametro *pValue* del metodo [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) se **WMT \_ status** è uguale a **WMT \_ No \_ Rights \_ ex** o **WMT \_ acquisisce \_ License**. Per gli \_ eventi WMT No \_ Rights \_ , il membro **HR** sarà la licenza NS e la licenza NS e la licenza \_ \_ \_ \_ \_ \_ OUTOFDATE o \_ i diritti di licenza NS e non \_ \_ corretti \_ . Uno di questi errori indica che è necessario acquisire una nuova licenza passando all'URL del membro **wszURL** .

Per WMT \_ Acquisisci gli \_ eventi di licenza, il membro **HR** PASSerà la macro SUCCEEDED se una licenza è stata acquisita correttamente. Se questo evento viene ricevuto dopo un tentativo di acquisizione invisibile all'utente e **HR** è uguale a NS \_ e \_ DRM \_ License \_ NOTACQUIRED, indica che il server licenze per questa licenza supporta solo l'acquisizione non invisibile all'utente.

Nell'applicazione di esempio AudioPlayer viene illustrato come utilizzare correttamente le informazioni restituite nella struttura.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                      |
| Versione<br/>                  | Windows Media Format 7 SDK o versioni successive dell'SDK<br/>                       |
| Intestazione<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWMDRMReader:: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense)
</dt> <dt>

[**Strutture**](structures.md)
</dt> </dl>

 

 





