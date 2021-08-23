---
description: Definisce i dati da usare nella verifica Microsoft Authenticode dei dati degli elementi.
ms.assetid: 73c0e84f-7d59-4efa-927d-af8d7305bc9d
title: PST_AUTHENTICODEDATA (Pstore.h)
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
ms.openlocfilehash: abf5bc69fd36e45cc715b3805f5407e821cfc7efc7f6595bcfc9eab8d762b716
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690861"
---
# <a name="pst_authenticodedata-structure"></a>Struttura \_ PST AUTHENTICODEDATA

\[Protected Archiviazione (Pstore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. Pstore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono fortemente invitati a sfruttare la protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Definisce i dati da usare nella verifica Microsoft Authenticode dei dati degli elementi.

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

Valore che identifica il modificatore che deve essere verificato da una catena di chiamanti.



| Valore                                                                                                                                                                                                                                                 | Significato                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PST_AC_SINGLE_CALLER"></span><span id="pst_ac_single_caller"></span><dl> <dt>**PST \_ AC \_ SINGLE \_ CALLER**</dt> <dt>0</dt> </dl>           | Solo un singolo livello nella catena di chiamate a PStore. Il chiamante supera il controllo di verifica. L'immagine specificata è il chiamante immediato ed è un'applicazione (.exe).<br/>              |
| <span id="PST_AC_TOP_LEVEL_CALLER"></span><span id="pst_ac_top_level_caller"></span><dl> <dt>**PST \_ AC \_ TOP \_ LEVEL \_ CALLER**</dt> <dt>1</dt> </dl> | Il chiamante di primo livello deve superare il controllo, ma potrebbero essere presenti DLL intermedie. L'immagine specificata non è necessariamente il chiamante immediato ed è un'applicazione (.exe).<br/>           |
| <span id="PST_AC_IMMEDIATE_CALLER"></span><span id="pst_ac_immediate_caller"></span><dl> <dt>**PST \_ AC \_ IMMEDIATE \_ CALLER**</dt> <dt>2</dt> </dl>  | Il chiamante immediato deve superare il controllo, ma non deve essere il processo di primo livello. L'immagine specificata è il chiamante immediato e l'immagine può essere un'applicazione (.exe) o una DLL.<br/> |



 

</dd> <dt>

**szRootCA**
</dt> <dd>

Puntatore a una stringa di caratteri wide che rappresenta l'autorità di certificazione radice (CA) per il certificato. usare **NULL per** usare qualsiasi AUTORITÀ di certificazione disponibile.

</dd> <dt>

**szIssuer**
</dt> <dd>

Puntatore a una stringa di caratteri wide che rappresenta la CA che ha emesso il certificato. usare **NULL per** usare qualsiasi AUTORITÀ di certificazione disponibile.

</dd> <dt>

**szPublisher**
</dt> <dd>

Puntatore a una stringa di caratteri wide che rappresenta l'autore del software. usare **NULL per** usare qualsiasi AUTORITÀ di certificazione disponibile.

</dd> <dt>

**szProgramName**
</dt> <dd>

Puntatore a una stringa di caratteri wide che rappresenta il nome del programma. usare **NULL per** usare qualsiasi AUTORITÀ di certificazione disponibile.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Pstore.h</dt> </dl> |



 

 
