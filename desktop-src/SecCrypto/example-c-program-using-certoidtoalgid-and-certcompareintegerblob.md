---
description: Nell'esempio seguente viene illustrato l'utilizzo delle funzioni CertOIDToAlgId e CertCompareIntegerBlob.
ms.assetid: 89186d98-80a9-460a-be2b-3e328675c485
title: 'Esempio di programma C: uso di CertOIDToAlgId e CertCompareIntegerBlob'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd7239dc8872d1330cfd0dc96b00bcc201f94e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966756"
---
# <a name="example-c-program-using-certoidtoalgid-and-certcompareintegerblob"></a>Esempio di programma C: uso di CertOIDToAlgId e CertCompareIntegerBlob

Nell'esempio seguente viene illustrato l'utilizzo delle funzioni [**CertOIDToAlgId**](/windows/desktop/api/Wincrypt/nf-wincrypt-certoidtoalgid) e [**CertCompareIntegerBlob**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcompareintegerblob) .

Per prima cosa, tutti i OID disponibili vengono enumerati usando [**CryptEnumOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumoidinfo). Il codice usato con questa funzione illustra anche l'uso di una funzione di callback. La funzione di callback Mostra la logica di interruzione per sospendere tra ogni gruppo OID e dopo aver presentato le informazioni su un numero set di OID.

In secondo luogo, tre stringhe dell' [*identificatore di oggetto*](../secgloss/o-gly.md) (OID) vengono convertite in integer con identificatore di algoritmo **DWORD** usando [**CertOIDToAlgId**](/windows/desktop/api/Wincrypt/nf-wincrypt-certoidtoalgid). Il codice dimostra anche che tutte le stringhe OID non hanno identificatori di algoritmo correlati.

Infine, nell'esempio viene illustrato il confronto dei BLOB di interi. In questo esempio viene illustrato il troncamento di 0x00's iniziali da numeri positivi e 0xFF's iniziali da numeri negativi.

Mostra anche che i numeri interi vengono confrontati come se fossero archiviati in formato [*Little-Endian*](../secgloss/l-gly.md) con le cifre più significative a destra.


```C++
#pragma comment(lib, "crypt32.lib")

#include <windows.h>
#include <stdio.h>
#include <Wincrypt.h>

//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// Declare a wait function to be defined following main.

void my_wait(char *s);

//-------------------------------------------------------------------
// Callback function to print information
// saved in each CRYPT_OID_INFO structure.
// This function counts the number of lines printed
// and does a wait for each new ground and after any four
// report groups are printed.

static BOOL WINAPI EnumInfoCallback(
     PCCRYPT_OID_INFO pInfo,
     void *pvArg
    )
{
static int old_oid = 0;
static int break_counter = 0;

if( old_oid < pInfo->dwGroupId)
{
     if(old_oid > 0)
     {
          my_wait("\n Begin new group. \n Hit enter to continue.");
          break_counter=0;
     }
     old_oid = pInfo->dwGroupId;
     printf("\nNew Group ID %d \n",old_oid);
}
printf("  OID: %s\n  Name: %S\n",
       pInfo->pszOID, pInfo->pwszName);

//-------------------------------------------------------------------
// If there is an AlgId, print it.

if( pInfo->Algid > 0)
{
     printf("  Algorithm ID hexadecimal %x \n\n",pInfo->Algid);
}
else
{
     printf("\n");
}

if(++break_counter > 4)
{ 
     break_counter = 0;
     my_wait("\n   Hit enter to continue.");
}
return TRUE;
}

void main()
{
//-------------------------------------------------------------------
// Note: Integer BLOBs are treated as if they
// are stored in little-endian form with the 
// most significant digits on the right. Truncation is 
// therefore from the right.
// Integer BLOBs are also assumed to be signed numbers
// in two's compliment form.
// For negative numbers, 0xFFs on the right are 
// truncated.
// For positive numbers, 0x00s on the right are 
// truncated.

//-------------------------------------------------------------------
// Declare and initialize local variables.

DWORD Alg_Id;
CRYPT_INTEGER_BLOB  Int1, Int2;
BYTE BLOB1data[4] = {0x88, 0xFF, 0xFF, 0xFF};
BYTE BLOB2data[2] = {0x88, 0xFF};
BYTE BLOB3data[4] = {0x01, 0x00, 0x00, 0x00};
BYTE BLOB4data[2] = {0x01, 0x00};
BYTE BLOB5data[4] = {0x01, 0x00, 0x01, 0x00};

//-------------------------------------------------------------------
// Enumerate the algorithm OIDs available.
// Note that this one call to the function with
// dwGroupId set to 0 lists all OIDs in all groups. 

if(!(CryptEnumOIDInfo(
    0,                  // use 0 to enumerate the OIDs in all groups
    0,                  // dwFlags
    NULL,               // no additional parameters are to be 
                        // passed to the callback function.
    EnumInfoCallback    // name of the callback function to be 
                        // called for each OID enumerated.
    )))
{
    printf("Enumeration of algorithm OIDs did not complete.\n");
}

//-------------------------------------------------------------------
// Use CertOIDToAlgId() to 
// convert the szOID_RSA_RC4 Object Identifier string to an 
// algorithm identifier.

if( Alg_Id = CertOIDToAlgId(szOID_RSA_RC4))
{
   // Print the Alg_Id returned in hex.
   printf("szOID_RSA_RC4 / %s is %x\n\n",szOID_RSA_RC4, Alg_Id);
}
else
{
   printf("No ALG_ID for OID szOID_RSA_RC4 / %s.\n", szOID_RSA_RC4);
}

//-------------------------------------------------------------------
// Convert the szOID_RSA_RC2CBC Object Identifier string to an 
// algorithm identifier.

if( Alg_Id = CertOIDToAlgId(szOID_RSA_RC2CBC))
{
   // Print the Alg_Id returned in hex.
   printf("szOID_RSA_RC2CBC / %s is %x\n\n",szOID_RSA_RC2CBC, 
      Alg_Id);
}
else
{
   printf("No ALG_ID for szOID_RSA_RC2CBC / %s.\n",szOID_RSA_RC2CBC);
}

//-------------------------------------------------------------------
// Convert the szOID_RSA_RC5_CBCPad Object Identifier string to an 
// algorithm identifier.

if( Alg_Id = CertOIDToAlgId(szOID_RSA_RC5_CBCPad))
{
   // Print the Alg_Id returned in hex.
   printf("szOID_RSA_RC5_CBCPad / %s is %x\n",szOID_RSA_RC5_CBCPad, 
      Alg_Id);
}
else
{
    printf("No ALG_ID for szOID_RSA_RC5_CBCPad: %s.\n",
      szOID_RSA_RC5_CBCPad);
}

//-------------------------------------------------------------------
// Initialize Int1 and Int2. 

Int1.pbData = (BYTE*)&BLOB1data;
Int2.pbData = (BYTE*)&BLOB2data;

//-------------------------------------------------------------------
// Set the cbData members so that only 
// the leftmost two bytes of the 
// first are compared to the leftmost bytes 
// of the second.

Int1.cbData = 4;  // sizeof(BLOB1data);
Int2.cbData = 2;  // sizeof(BLOB2data);

if( CertCompareIntegerBlob(
     &Int1, 
     &Int2))
{
   printf("The first two bytes of the BLOBs are identical.\n");
}
else
{
   printf("The first two bytes BLOBs are not identical.\n");
}

//-------------------------------------------------------------------
// Reset the cbData members to compare only 
// 1 byte from each.

Int1.cbData=1;
Int2.cbData=1;

if( CertCompareIntegerBlob(
       &Int1, 
       &Int2))
{
    printf("The BLOBs of different length are identical.\n");
}
else
{
    printf("The BLOBs of different length are not identical.\n");
}

//-------------------------------------------------------------------
// Reset to check the positive numbers.

Int1.cbData = 4;
Int2.cbData = 2;
Int1.pbData = BLOB3data;
Int2.pbData = BLOB4data;

if( CertCompareIntegerBlob(
       &Int1, 
       &Int2))
{
   printf("The BLOBs 3 and 4 are identical.\n");
}
else
{
   printf("The BLOBs 3 and 4 are not identical.\n");
}

//-------------------------------------------------------------------
// Compare BLOB 1 and BLOB 3.

Int1.cbData = 4;
Int2.cbData = 4;
Int1.pbData = BLOB1data;
Int2.pbData = BLOB3data;

if( CertCompareIntegerBlob(
       &Int1, 
       &Int2))
{
   printf("BLOBs 1 and 3 are identical.\n");
}
else
{
   printf("BLOBs 1 and 3 are not identical.\n");
}

//-------------------------------------------------------------------
// Compare BLOB 3 and BLOB 5.

Int1.cbData = 4;
Int2.cbData = 4;
Int1.pbData = BLOB5data;
Int2.pbData = BLOB3data;

if( CertCompareIntegerBlob(
       &Int1, 
       &Int2))
{
   printf("BLOBs 5 and 3 are identical.\n");
}
else
{
   printf("BLOBs 5 and 3 are not identical.\n");
}

//-------------------------------------------------------------------
// Compare the first two bytes of BLOB 3 and BLOB 5.

Int1.cbData = 2;
Int2.cbData = 2;
Int1.pbData = BLOB5data;
Int2.pbData = BLOB3data;

if( CertCompareIntegerBlob(
       &Int1, 
       &Int2))
{
   printf("The first two bytes of BLOBs 5 and 3 are identical.\n");
}
else
{
   printf("The first two bytes of BLOBs 5 and 3 not identical.\n");
}
} // end main

//-------------------------------------------------------------------
// Define the my_wait function.
void my_wait(char* s)
{
     printf(s);
     getchar();
}
```



 

 
