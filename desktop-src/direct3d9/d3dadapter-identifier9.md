---
description: Contiene informazioni che identificano l'adapter.
ms.assetid: d0d59df9-c512-4d69-b0a0-7d87d7a380f6
title: D3DADAPTER_IDENTIFIER9 struttura (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DADAPTER_IDENTIFIER9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 85401573956d29386b5ddabbd48711a7be140463
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129970"
---
# <a name="d3dadapter_identifier9-structure"></a>Struttura D3DADAPTER \_ IDENTIFIER9

Contiene informazioni che identificano l'adapter.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DADAPTER_IDENTIFIER9 {
  char          Driver[MAX_DEVICE_IDENTIFIER_STRING];
  char          Description[MAX_DEVICE_IDENTIFIER_STRING];
  char          DeviceName[32];
#ifdef _WIN32
  LARGE_INTEGER DriverVersion;
#else
  DWORD         DriverVersionLowPart;
  DWORD         DriverVersionHighPart;
#endif
  DWORD         VendorId;
  DWORD         DeviceId;
  DWORD         SubSysId;
  DWORD         Revision;
  GUID          DeviceIdentifier;
  DWORD         WHQLLevel;
} D3DADAPTER_IDENTIFIER9, *LPD3DADAPTER_IDENTIFIER9;
```



## <a name="members"></a>Members

<dl> <dt>

**Driver**
</dt> <dd>

Tipo: **char**

</dd> <dd>

Usato per la presentazione all'utente. Questo non deve essere usato per identificare driver specifici, perché molte stringhe diverse potrebbero essere associate allo stesso dispositivo e driver di fornitori diversi.

</dd> <dt>

**Descrizione**
</dt> <dd>

Tipo: **char**

</dd> <dd>

Usato per la presentazione all'utente.

</dd> <dt>

**DeviceName**
</dt> <dd>

Tipo: **char**

</dd> <dd>

Nome del dispositivo per GDI.

</dd> <dt>

**DriverVersion**
</dt> <dd>

Tipo: **[ **LARGE \_ INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**

</dd> <dd>

Identificare la versione del driver Direct3D. È legale eseguire confronti minori e maggiori di sul valore intero con segno a 64 bit. Prestare tuttavia attenzione se si usa questo elemento per identificare i driver problematici. È invece consigliabile usare DeviceIdentifier. Vedere la sezione Osservazioni.

</dd> <dt>

**DriverVersionLowPart**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Identificare la versione del driver Direct3D. È legale eseguire confronti < e > sul valore intero con segno a 64 bit. Prestare tuttavia attenzione se si usa questo elemento per identificare i driver problematici. È invece consigliabile usare DeviceIdentifier. Vedere la sezione Osservazioni.

</dd> <dt>

**DriverVersionHighPart**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Identificare la versione del driver Direct3D. È legale eseguire confronti < e > sul valore intero con segno a 64 bit. Prestare tuttavia attenzione se si usa questo elemento per identificare i driver problematici. È invece consigliabile usare DeviceIdentifier. Vedere la sezione Osservazioni.

</dd> <dt>

**VendorId**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Può essere usato per identificare un determinato chip set. Eseguire una query su questo membro per identificare il produttore. Il valore può essere zero se sconosciuto.

</dd> <dt>

**DeviceId**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Può essere usato per identificare un determinato chip set. Eseguire una query su questo membro per identificare il tipo di chip set. Il valore può essere zero se sconosciuto.

</dd> <dt>

**SubSysId**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Può essere usato per identificare un determinato chip set. Eseguire una query su questo membro per identificare il sottosistema, in genere la scheda specifica. Il valore può essere zero se sconosciuto.

</dd> <dt>

**Revisione**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Può essere usato per identificare un determinato chip set. Eseguire una query su questo membro per identificare il livello di revisione del chip set. Il valore può essere zero se sconosciuto.

</dd> <dt>

**DeviceIdentifier**
</dt> <dd>

Tipo: **[ **GUID**](guid.md)**

</dd> <dd>

È possibile eseguire query per controllare le modifiche nel driver e nel chip set. Questo GUID è un identificatore univoco per la coppia di driver e chip set. Eseguire una query su questo membro per tenere traccia delle modifiche apportate al driver e al chip set per generare un nuovo profilo per il sottosistema grafico. DeviceIdentifier può essere usato anche per identificare driver problematici specifici.

</dd> <dt>

**WHQLLevel**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Usato per determinare il Windows Hardware Quality Labs di convalida (WHQL) per questa coppia di driver e dispositivo. Il valore DWORD è una struttura di data di tipo pack che definisce la data di rilascio del test WHQL più recente superato dal driver. È legale eseguire operazioni < e > su questo valore. Di seguito viene illustrato il formato della data.



| BITS  |  Descrizione                                             |
|-------|-----------------------------------------------|
| 31-16 | Anno, un numero decimale dal 1999 verso l'alto. |
| 15-8  | Mese, numero decimale da 1 a 12.     |
| 7-0   | Giorno, numero decimale da 1 a 31.       |



 

Vengono usati anche i valori seguenti.



| Valore    |  Descrizione                                                     |
|-----|-------------------------------------------------------|
| 0   | Non certificata.                                        |
| 1   | WHQL convalidato, ma non sono disponibili informazioni sulla data. |



 

Differenze tra Direct3D 9 e Direct3D 9Ex:

Per Direct3D9Ex in esecuzione in Windows Vista, Windows Server 2008, Windows 7 e Windows Server 2008 R2 (o un sistema operativo più recente), [**IDirect3D9::GetAdapterIdentifier**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) restituisce 1 per il livello WHQL senza controllare lo stato del driver.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'esempio di pseudocodice seguente illustra il formato della versione codificato nei membri DriverVersion, DriverVersionLowPart e DriverVersionHighPart.


```
Product = HIWORD(DriverVersion.HighPart)
Version = LOWORD(DriverVersion.HighPart)
SubVersion = HIWORD(DriverVersion.LowPart)
Build = LOWORD(DriverVersion.LowPart)
```



Per altre informazioni sulla macro HIWORD, sulla macro LOWORD e sulla struttura LARGE INTEGER, vedere Platform \_ SDK.

MAX \_ DEVICE IDENTIFIER STRING è una costante con la definizione \_ \_ seguente.


```
#define MAX_DEVICE_IDENTIFIER_STRING        512
```



I membri VendorId, DeviceId, SubSysId e Revision possono essere usati in tandem per identificare determinati chip set. Tuttavia, usare questi membri con cautela.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
