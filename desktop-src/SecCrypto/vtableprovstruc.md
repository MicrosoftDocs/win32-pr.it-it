---
description: Contiene puntatori a funzioni di callback che possono essere usate dalle funzioni del provider del servizio di crittografia (CSP).
ms.assetid: 84a379e9-c6b9-4c1d-bbbb-9bed4a045d90
title: Struttura VTableProvStruc (Cspdk.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VTableProvStruc
- VTableProvStrucW
api_type:
- HeaderDef
api_location:
- Cspdk.h
ms.openlocfilehash: 2815d12735023cd0f7ac60fc2ed9f60fc56e32d0f54610f295a2e6b0544e589c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117970867"
---
# <a name="vtableprovstruc-structure"></a>Struttura VTableProvStruc

La **struttura VTableProvStruc** contiene puntatori a funzioni di callback che possono essere usate dalle funzioni CSP [*(Cryptographic Service Provider).*](../secgloss/c-gly.md)

## <a name="syntax"></a>Sintassi


```C++
typedef struct VTableProvStruc {
  DWORD   Version;
  FARPROC FuncVerifyImage;
  FARPROC FuncReturnhWnd;
  DWORD   dwProvType;
  BYTE    *pbContextInfo;
  DWORD   cbContextInfo;
  LPSTR   pszProvName;
} VTableProvStruc, *PVTableProvStruc;
```



## <a name="members"></a>Members

<dl> <dt>

**Version**
</dt> <dd>

Valore **DWORD** che indica la versione della struttura . Vengono usate tre versioni di questa struttura. Le versioni sono i numeri 1, 2 e 3 e determinano quali membri della struttura sono validi. I membri della versione 1 sono validi in tutti i sistemi che supportano questa struttura.

Si tratta di un membro della versione 1.

</dd> <dt>

**FuncVerifyImage**
</dt> <dd>

Indirizzo di una funzione di callback [**FuncVerifyImage**](funcverifyimage.md) che il CSP usa per verificare la firma di tutte le DLL che verranno caricate dal CSP. Tutte le DLL ausiliarie in cui un CSP effettua chiamate di funzione devono essere firmate nello stesso modo (e con la stessa chiave) della DLL CSP primaria. Per garantire questa firma, le DLL ausiliarie devono essere caricate dinamicamente usando la [**funzione LoadLibrary.**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) Tuttavia, prima del caricamento della DLL, è necessario verificare la firma della DLL. Il CSP esegue questa verifica chiamando la **funzione FuncVerifyImage,** come illustrato nell'esempio seguente.

Questo puntatore a funzione può essere archiviato e usato fino al rilascio del contesto CSP.

Si tratta di un membro della versione 1.

</dd> <dt>

**FuncReturnhWnd**
</dt> <dd>

Indirizzo di una funzione di callback [**FuncReturnhWnd**](funcreturnhwnd.md) che restituisce l'handle di finestra che il CSP deve usare come padre o proprietario di qualsiasi interfaccia utente visualizzata. I CSP che non comunicano direttamente con l'utente e i CSP che usano hardware dedicato a questo scopo possono ignorare questa voce. Questo handle di finestra è zero per impostazione predefinita, ma un'applicazione può impostarlo su un valore diverso usando la funzione [**CryptSetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovparam) per impostare la proprietà **PP CLIENT \_ \_ HWND.**

Questo puntatore a funzione può essere archiviato e usato fino al rilascio del contesto CSP.

Si tratta di un membro della versione 1.

</dd> <dt>

**dwProvType**
</dt> <dd>

Valore **DWORD** che specifica il tipo di provider da acquisire. I tipi [*di provider seguenti*](../secgloss/p-gly.md) sono predefiniti e vengono descritti in dettaglio in [Interoperabilità CSP:](https://www.bing.com/search?q=CSP+Interoperability)

-   PROV \_ RSA \_ FULL
-   PROV \_ RSA \_ SIG
-   PROV \_ DSS
-   PROV \_ FORTARE
-   PROV \_ MS \_ EXCHANGE

Si tratta di un membro della versione 2.

</dd> <dt>

**pbContextInfo**
</dt> <dd>

Puntatore a una matrice di informazioni di contesto. I **membri pbContextInfo** e **cbContextInfo** determinano insieme il set di informazioni usato quando viene chiamata una funzione [**CPSetProvParam**](https://www.bing.com/search?q=**CPSetProvParam**) con PP \_ CONTEXT INFO \_ impostato.

Si tratta di un membro della versione 2.

</dd> <dt>

**cbContextInfo**
</dt> <dd>

Valore **DWORD** che indica il numero di elementi nella matrice **pbContextInfo.**

Si tratta di un membro della versione 2.

</dd> <dt>

**pszProvName**
</dt> <dd>

Stringa contenente il nome del provider.

Si tratta di un membro della versione 3.

</dd> </dl>

## <a name="remarks"></a>Commenti

I puntatori nella **struttura VTableProvStruc** sono disponibili solo all'interno della [**funzione CPAcquireContext.**](https://www.bing.com/search?q=**CPAcquireContext**) Se i membri della struttura sono necessari dopo il completamento di una chiamata a **CPAcquireContext,** il CSP deve creare copie degli elementi della struttura necessari. I puntatori a funzione in questa struttura possono essere archiviati e usati fino al rilascio del contesto CSP.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Cspdk.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **VTableProvStrucW** (Unicode)<br/>                                          |



 

 
