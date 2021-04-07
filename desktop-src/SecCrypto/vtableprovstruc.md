---
description: Contiene i puntatori alle funzioni di callback che possono essere utilizzati dalle funzioni del provider del servizio di crittografia (CSP).
ms.assetid: 84a379e9-c6b9-4c1d-bbbb-9bed4a045d90
title: Struttura VTableProvStruc (Cspdk. h)
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
ms.openlocfilehash: 99b9344c6951dc93972315d9b4f60752f1484d68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759458"
---
# <a name="vtableprovstruc-structure"></a>Struttura VTableProvStruc

La struttura **VTableProvStruc** contiene i puntatori alle funzioni di callback che possono essere utilizzati dalle funzioni del [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP).

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

**Versione**
</dt> <dd>

Valore **DWORD** che indica la versione della struttura. Vengono utilizzate tre versioni di questa struttura. Le versioni sono il numero 1, 2 e 3 e determinano quali membri della struttura sono validi. I membri della versione 1 sono validi in tutti i sistemi che supportano questa struttura.

Si tratta di un membro della versione 1.

</dd> <dt>

**FuncVerifyImage**
</dt> <dd>

Indirizzo di una funzione di callback [**FuncVerifyImage**](funcverifyimage.md) che il CSP utilizza per verificare la firma di tutte le dll che il CSP caricherà. Tutte le DLL ausiliarie in cui un CSP effettua chiamate di funzione devono essere firmate nello stesso modo (e con la stessa chiave) della DLL CSP primaria. Per garantire la firma, le DLL ausiliarie devono essere caricate in modo dinamico tramite la funzione [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) . Ma prima del caricamento della DLL, è necessario verificare la firma della DLL. Il CSP esegue questa verifica chiamando la funzione **FuncVerifyImage** , come illustrato nell'esempio riportato di seguito.

Questo puntatore a funzione può essere archiviato e utilizzato fino a quando non viene rilasciato il contesto CSP.

Si tratta di un membro della versione 1.

</dd> <dt>

**FuncReturnhWnd**
</dt> <dd>

Indirizzo di una funzione di callback [**FuncReturnhWnd**](funcreturnhwnd.md) che restituisce l'handle della finestra che deve essere utilizzato dal CSP come padre o proprietario di qualsiasi interfaccia utente visualizzata. I CSP che non comunicano direttamente con l'utente e i CSP che utilizzano hardware dedicato a questo scopo possono ignorare questa voce. Questo handle di finestra è pari a zero per impostazione predefinita, ma un'applicazione può impostarla su un valore diverso usando la funzione [**CryptSetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovparam) per impostare la proprietà **\_ \_ HWND del client PP** .

Questo puntatore a funzione può essere archiviato e utilizzato fino a quando non viene rilasciato il contesto CSP.

Si tratta di un membro della versione 1.

</dd> <dt>

**dwProvType**
</dt> <dd>

Valore **DWORD** che specifica il tipo di provider da acquisire. I [*tipi di provider*](../secgloss/p-gly.md) seguenti sono predefiniti e sono descritti in dettaglio nell' [interoperabilità CSP](https://www.bing.com/search?q=CSP+Interoperability):

-   PROV \_ RSA \_ completo
-   PROVA \_ RSA \_ sig
-   PROVA \_ DSS
-   PROVA \_ fortezza
-   PROVA \_ MS \_ Exchange

Si tratta di un membro della versione 2.

</dd> <dt>

**pbContextInfo**
</dt> <dd>

Puntatore a una matrice di informazioni di contesto. I membri **pbContextInfo** e **cbContextInfo** determinano il set di informazioni usato quando viene chiamata una funzione [**CPSetProvParam**](https://www.bing.com/search?q=**CPSetProvParam**) con le informazioni sul \_ contesto PP \_ impostate.

Si tratta di un membro della versione 2.

</dd> <dt>

**cbContextInfo**
</dt> <dd>

Valore **DWORD** che indica il numero di elementi nella matrice **pbContextInfo** .

Si tratta di un membro della versione 2.

</dd> <dt>

**pszProvName**
</dt> <dd>

Stringa che contiene il nome del provider.

Si tratta di un membro della versione 3.

</dd> </dl>

## <a name="remarks"></a>Commenti

I puntatori nella struttura **VTableProvStruc** sono disponibili solo all'interno della funzione [**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**) . Se i membri della struttura sono necessari dopo il completamento di una chiamata a **CPAcquireContext** , le copie degli elementi della struttura necessari devono essere eseguite dal CSP. I puntatori a funzione in questa struttura possono essere archiviati e utilizzati fino a quando non viene rilasciato il contesto CSP.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Cspdk. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **VTableProvStrucW** (Unicode)<br/>                                          |



 

 
