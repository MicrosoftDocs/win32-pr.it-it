---
description: Questa sezione elenca i valori usati per la funzionalità di connessione a banda larga.
ms.assetid: 9e45ca17-2aec-42e5-88a5-5ef1dc4238d9
title: Funzionalità di connessione a banda larga
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f1294724726d766c209c9f83adc5dd2bfc0db2680cf144759b95654748b0d81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118560329"
---
# <a name="broadband-bearer-capability"></a>Funzionalità di connessione a banda larga

Questa sezione elenca i valori usati per la funzionalità di connessione a banda larga.

``` syntax
#include <windows.h>

/* 
 *  values used for the BearerClass field in struct ATM_BROADBAND_BEARER_CAPABILITY_IE
 */
#define BCOB_A                   0x00   /* Bearer class A           */
#define BCOB_C                   0x03   /* Bearer class C           */
#define BCOB_X                   0x10   /* Bearer class X           */

/* 
 *  values used for the TrafficType field in struct ATM_BROADBAND_BEARER_CAPABILITY_IE
 */
#define TT_NOIND                 0x00   /* No indication of traffic type       */
#define TT_CBR                   0x04   /* Constant bit rate                   */
#define TT_VBR                   0x06   /* Variable bit rate                   */

/* 
 *  values used for the TimingRequirements field in struct ATM_BROADBAND_BEARER_CAPABILITY_IE
 */
#define TR_NOIND                 0x00   /* No timing requirement indication    */
#define TR_END_TO_END            0x01   /* End-to-end timing required          */
#define TR_NO_END_TO_END         0x02   /* End-to-end timing not required      */

/* 
 *  values used for the ClippingSusceptability field in struct ATM_BROADBAND_BEARER_CAPABILITY_IE
 */
#define CLIP_NOT                 0x00   /* Not susceptible to clipping         */
#define CLIP_SUS                 0x20   /* Susceptible to clipping             */

/* 
 *  values used for the UserPlaneConnectionConfig field in 
 *  struct ATM_BROADBAND_BEARER_CAPABILITY_IE
 */
#define UP_P2P                   0x00   /* Point-to-point connection           */
#define UP_P2MP                  0x01   /* Point-to-multipoint connection      */

typedef struct {
    UCHAR BearerClass;
    UCHAR TrafficType;
    UCHAR TimingRequirements;
    UCHAR ClippingSusceptability;
    UCHAR UserPlaneConnectionConfig;
} ATM_BROADBAND_BEARER_CAPABILITY_IE;
```

 

 



