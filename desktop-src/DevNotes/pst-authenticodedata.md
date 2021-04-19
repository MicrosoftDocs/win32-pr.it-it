---
description: Definisce i dati da utilizzare nella verifica Microsoft Authenticode dei dati dell'elemento.
ms.assetid: 73c0e84f-7d59-4efa-927d-af8d7305bc9d
title: Struttura PST_AUTHENTICODEDATA (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_AUTHENTICODEDATA
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: ff53526febcc8eab1a95285ffa3dcb59fe628238
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328038"
---
# <a name="pst_authenticodedata-structure"></a>\_Struttura AUTHENTICODEDATA PST

\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. PStore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Definisce i dati da utilizzare nella verifica Microsoft Authenticode dei dati dell'elemento.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD    cbSize;
  DWORD    dwModifiers;
  LPCWSTR  szRootCA;
  LPCWSTR  szIssuer;
  LPCWSTR  szPublisher;
  LPCWSTR  szProgramName;
} PST_AUTHENTICODEDATA, *PPST_AUTHENTICODE_DATA;
```



## <a name="members"></a>Members

<dl> <dt>

**cbSize**
</dt> <dd>

Dimensione della struttura.

</dd> <dt>

**dwModifiers**
</dt> <dd>

Valore che identifica il modificatore che una di una catena di chiamanti deve verificare.



| Valore                                                                                                                                                                                                                                                 | Significato                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PST_AC_SINGLE_CALLER"></span><span id="pst_ac_single_caller"></span><dl> <dt>**Pst \_ \_Singolo \_ chiamante AC**</dt> <dt>0</dt> </dl>           | Solo un singolo livello nella catena di chiamate a PStore. Il chiamante supera il controllo di verifica. L'immagine specificata è il chiamante immediato e è un'applicazione (exe).<br/>              |
| <span id="PST_AC_TOP_LEVEL_CALLER"></span><span id="pst_ac_top_level_caller"></span><dl> <dt>**Pst \_ \_Chiamante di \_ livello \_ superiore AC**</dt> <dt>1</dt> </dl> | Il chiamante di livello superiore deve superare il controllo, ma potrebbero essere presenti dll intermedie. L'immagine specificata non è necessariamente il chiamante immediato e è un'applicazione (exe).<br/>           |
| <span id="PST_AC_IMMEDIATE_CALLER"></span><span id="pst_ac_immediate_caller"></span><dl> <dt>**Pst \_ \_ \_ Chiamante immediato AC**</dt> <dt>2</dt> </dl>  | Il chiamante immediato deve superare il controllo, ma non deve essere il processo di primo livello. L'immagine specificata è il chiamante immediato e l'immagine può essere un'applicazione (con estensione exe) o una DLL.<br/> |



 

</dd> <dt>

**szRootCA**
</dt> <dd>

Puntatore a una stringa di caratteri wide che rappresenta l'autorità di certificazione radice (CA) per il certificato. usare **null** per usare un'autorità di certificazione disponibile.

</dd> <dt>

**szIssuer**
</dt> <dd>

Puntatore a una stringa di caratteri wide che rappresenta l'autorità di certificazione che ha emesso il certificato. usare **null** per usare un'autorità di certificazione disponibile.

</dd> <dt>

**szPublisher**
</dt> <dd>

Puntatore a una stringa di caratteri wide che rappresenta l'autore del software; usare **null** per usare un'autorità di certificazione disponibile.

</dd> <dt>

**szProgramName**
</dt> <dd>

Puntatore a una stringa di caratteri wide che rappresenta il nome del programma; usare **null** per usare un'autorità di certificazione disponibile.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PStore. h</dt> </dl> |



 

 
