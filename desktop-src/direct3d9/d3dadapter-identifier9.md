---
description: Contiene informazioni che identificano l'adapter.
ms.assetid: d0d59df9-c512-4d69-b0a0-7d87d7a380f6
title: Struttura D3DADAPTER_IDENTIFIER9 (D3D9Types. h)
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
ms.openlocfilehash: 33aba75cafff5f9e69a74d5570f98455a9853289
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322381"
---
# <a name="d3dadapter_identifier9-structure"></a>\_Struttura D3DADAPTER IDENTIFIER9

Contiene informazioni che identificano l'adapter.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DADAPTER_IDENTIFIER9 {
  char          Driver[MAX_DEVICE_IDENTIFIER_STRING];
  char          Description[MAX_DEVICE_IDENTIFIER_STRING];
  char          DeviceName[32];
  LARGE_INTEGER DriverVersion;
  DWORD         DriverVersionLowPart;
  DWORD         DriverVersionHighPart;
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

Utilizzato per la presentazione all'utente. Questa operazione non deve essere utilizzata per identificare driver specifici, perché molte stringhe diverse possono essere associate allo stesso dispositivo e driver di fornitori diversi.

</dd> <dt>

**Descrizione**
</dt> <dd>

Tipo: **char**

</dd> <dd>

Utilizzato per la presentazione all'utente.

</dd> <dt>

**DeviceName**
</dt> <dd>

Tipo: **char**

</dd> <dd>

Nome del dispositivo per GDI.

</dd> <dt>

**DriverVersion**
</dt> <dd>

Tipo: **[ **\_ Integer grande**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**

</dd> <dd>

Identificare la versione del driver Direct3D. È possibile eseguire confronti minori di e superiori rispetto al valore Signed Integer a 64 bit. Tuttavia, prestare attenzione se si utilizza questo elemento per identificare i driver problematici. È invece consigliabile usare DeviceIdentifier. Vedere la sezione Osservazioni.

</dd> <dt>

**DriverVersionLowPart**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Identificare la versione del driver Direct3D. È lecito eseguire confronti < e > sul valore intero con segno a 64 bit. Tuttavia, prestare attenzione se si utilizza questo elemento per identificare i driver problematici. È invece consigliabile usare DeviceIdentifier. Vedere la sezione Osservazioni.

</dd> <dt>

**DriverVersionHighPart**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Identificare la versione del driver Direct3D. È lecito eseguire confronti < e > sul valore intero con segno a 64 bit. Tuttavia, prestare attenzione se si utilizza questo elemento per identificare i driver problematici. È invece consigliabile usare DeviceIdentifier. Vedere la sezione Osservazioni.

</dd> <dt>

**VendorId**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Può essere utilizzato per identificare un particolare set di chip. Eseguire una query su questo membro per identificare il produttore. Il valore può essere zero se sconosciuto.

</dd> <dt>

**DeviceId**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Può essere utilizzato per identificare un particolare set di chip. Eseguire una query su questo membro per identificare il tipo di set di chip. Il valore può essere zero se sconosciuto.

</dd> <dt>

**SubSysId**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Può essere utilizzato per identificare un particolare set di chip. Eseguire una query su questo membro per identificare il sottosistema, in genere la bacheca particolare. Il valore può essere zero se sconosciuto.

</dd> <dt>

**Revisione**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Può essere utilizzato per identificare un particolare set di chip. Eseguire una query su questo membro per identificare il livello di revisione del set di chip. Il valore può essere zero se sconosciuto.

</dd> <dt>

**DeviceIdentifier**
</dt> <dd>

Tipo: **[ **GUID**](guid.md)**

</dd> <dd>

È possibile eseguire una query per verificare le modifiche apportate al driver e al set di chip. Questo GUID è un identificatore univoco per la coppia di driver e set di chip. Eseguire una query su questo membro per tenere traccia delle modifiche al driver e al set di chip per generare un nuovo profilo per il sottosistema grafico. DeviceIdentifier può essere usato anche per identificare driver problematici particolari.

</dd> <dt>

**WHQLLevel**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Utilizzato per determinare il livello di convalida di Windows Hardware Quality Labs (WHQL) per questa coppia di driver e dispositivi. DWORD è una struttura di data compressa che definisce la data di rilascio del test WHQL più recente passato dal driver. È consentito eseguire operazioni di < e > su questo valore. Di seguito viene illustrato il formato della data.



|       |                                               |
|-------|-----------------------------------------------|
| BITS  |                                               |
| 31-16 | Anno, un numero decimale compreso tra 1999 e verso l'alto. |
| 15-8  | Il mese, un numero decimale compreso tra 1 e 12.     |
| 7-0   | Il giorno, un numero decimale compreso tra 1 e 31.       |



 

Vengono inoltre utilizzati i valori seguenti.



|     |                                                       |
|-----|-------------------------------------------------------|
| 0   | Non certificata.                                        |
| 1   | WHQL convalidato, ma non sono disponibili informazioni sulla data. |



 

Differenze tra Direct3D 9 e Direct3D 9Ex:

Per Direct3D9Ex in esecuzione in Windows Vista, Windows Server 2008, Windows 7 e Windows Server 2008 R2 (o più sistemi operativi correnti), [**IDirect3D9:: GetAdapterIdentifier**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) restituisce 1 per il livello WHQL senza controllare lo stato del driver.

</dd> </dl>

## <a name="remarks"></a>Commenti

Nell'esempio di pseudocodice seguente viene illustrato il formato della versione codificato nei membri DriverVersion, DriverVersionLowPart e DriverVersionHighPart.


```
Product = HIWORD(DriverVersion.HighPart)
Version = LOWORD(DriverVersion.HighPart)
SubVersion = HIWORD(DriverVersion.LowPart)
Build = LOWORD(DriverVersion.LowPart)
```



Per ulteriori informazioni sulla macro HIWORD, sulla macro LOWORD e sulla struttura di tipo Integer grande, vedere Platform SDK \_ .

\_ \_ \_ La stringa dell'identificatore di dispositivo Max è una costante con la definizione seguente.


```
#define MAX_DEVICE_IDENTIFIER_STRING        512
```



I membri VendorId, DeviceId, SubSysId e Revision possono essere utilizzati in combinazione per identificare determinati set di chip. Tuttavia, usare questi membri con cautela.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
